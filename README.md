# RUN_QUERY_TO_i-LINK
---Select : sub_group_list.lab_items_code||HOSxp||

SELECT
lab_items_sub_group_list.lab_items_code,
lab_items.lab_items_code,
lab_items_sub_group_list.lab_items_sub_group_code,
lab_items.lab_items_name,
lab_items.ecode,
lab_items.display_order
FROM
lab_items_sub_group_list
INNER JOIN lab_items ON lab_items.lab_items_code = lab_items_sub_group_list.lab_items_code
WHERE
lab_items_sub_group_list.lab_items_sub_group_code = ---80
ORDER BY
lab_items.display_order ASC
