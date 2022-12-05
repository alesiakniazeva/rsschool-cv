# Alesia Kniazeva

## Contacts

- E-mail: **alice.xx.green@gmail.com**
- Telegram: **@TracerMaker2077**
- Discord: **alesiakniazeva#7723**

## About Me

Hello, my name's Alesia Kniazeva. I work as a software engineer in one of the biggest telecommunication companies in Belarus. I develop applications for internal needs of company
using Delphi, MySQL, MS SQL.
Also I've been working as web-designer and marketer on freelance since 2020. I've been
creating landing pages prototypes and design.
My key strengths are patience, purposefulness and thirst for knowledge.

## Skills

- Figma
- Photoshop
- UX/UI Design
- User Research & Prototyping
- Delphi
- MySql
- MS SQL
- HTML&CSS Basics
- Github
- English level - B1

## Code Examples

```
SELECT  itog4.m_id, itog4.m_d_id, devicesname_tbl.dn_id, devicesname_tbl.dn_namedev, device_tbl.d_inv,
			device_tbl.d_sn, device_tbl.d_mac, itog4.m_date, itog4.m_i_id, invoices_tbl.i_it_id,
            invoicetype_tbl.it_nametype,
            IF(invoices_tbl.i_it_id = 1 OR invoices_tbl.i_it_id = 4, 'На складе', IF(invoices_tbl.i_it_id = 2, 'Списано/область', IF (invoices_tbl.i_it_id = 3, 'Передано на установку', 'В ремонте' ))) AS stat,
            itog4.m_mol_id, mol_tbl.mol_name, itog4.m_robj_id, itog4.m_rpodr_id,
            rec_obj.r_name AS r_name_obj, rec_podr.r_name AS r_name_podr, itog4.m_p_id, places_tbl.p_name, itog4.m_recfio

	FROM (
SELECT moving3.m_id, moving3.m_d_id, moving3.m_date, moving3.m_i_id, moving3.m_mol_id, moving3.m_robj_id, moving3.m_rpodr_id,
		moving3.m_p_id, moving3.m_recfio FROM
( SELECT MAX(moving2.m_id) AS max_id FROM
	(SELECT
        m1.m_d_id, MAX(m1.m_date) AS max_date
     FROM moving_tbl m1
     WHERE
		m1.m_del = 0

     GROUP BY m1.m_d_id
	) AS itog
    JOIN (SELECT m2.m_id, m2.m_d_id, m2.m_date
		  FROM moving_tbl m2
		  WHERE
				m2.m_del = 0

          ) AS moving2 ON moving2.m_d_id = itog.m_d_id AND moving2.m_date = itog.max_date
	GROUP BY moving2.m_d_id
) AS itog3
JOIN (SELECT m3.m_id, m3.m_d_id, m3.m_date, m3.m_count, m3.m_mol_id, m3.m_i_id, m3.m_robj_id, m3.m_rpodr_id, m3.m_p_id, m3.m_recfio
	  FROM moving_tbl m3
	  WHERE
			m3.m_del = 0

	 ) AS moving3 ON moving3.m_id = itog3.max_id ) AS itog4
JOIN device_tbl ON device_tbl.d_id = itog4.m_d_id AND device_tbl.d_del =0
JOIN devicesname_tbl ON devicesname_tbl.dn_id = device_tbl.d_dn_id AND devicesname_tbl.dn_del = 0
JOIN invoices_tbl ON invoices_tbl.i_id = itog4.m_i_id AND invoices_tbl.i_del =0
JOIN invoicetype_tbl ON invoicetype_tbl.it_id = invoices_tbl.i_it_id AND invoicetype_tbl.it_del=0
JOIN mol_tbl ON mol_tbl.mol_id = itog4.m_mol_id AND mol_tbl.mol_del = 0
LEFT JOIN recipients_tbl AS rec_obj ON rec_obj.r_id = itog4.m_robj_id AND rec_obj.r_del=0 AND rec_obj.r_ispodr = 0
LEFT JOIN recipients_tbl AS rec_podr ON rec_podr.r_id = itog4.m_rpodr_id AND rec_podr.r_del=0 IS NULL AND rec_podr.r_ispodr = 1
LEFT JOIN places_tbl ON places_tbl.p_id = itog4.m_p_id AND places_tbl.p_del=0
```

## Work Positions

1. December 2020 - June 2022: Web-designer, self-employed
2. June 2022 - Now: Software Engineer at Beltelecom

### Some of my design projects

https://www.behance.net/gallery/141019759/dizajn-lendinga-dlja-zapuska-kursa-po-zhenstvennosti

https://www.behance.net/gallery/139906103/dizajn-lendinga-dlja-zapuska-kursa-po-tovarnomu-biznesu

https://www.behance.net/gallery/112605485/landing-page-for-kitchen-production

## Education

2016-2021: BSU, Physics Faculty, Department of theoretical physics and astrophysics
