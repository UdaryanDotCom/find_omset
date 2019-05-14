# find_omset
cari jumlah omset
/**query   omset**/
SELECT [FICMISDATE]
        ,[KODECABANGBARU]
      ,[NAMACABANG]
        ,[TGLLPENCAIRAN]
				,NOLOAN
				  ,[LOANTYPE]
      ,[TANGGAL_PERPANJANG]
      ,[KOLBSM]
      ,[KOLCIF]
	  ,[PENCAIRANPOKOKLCY]
	  		 ,OSPOKOKLCY
			 	        FROM [pawning].[dbo].[2019-05-12.PencairanPembiayaan]
  where LOANTYPE IN('MUR0011','MUR0013','MUR0014','MUR0016','MUR0018','RHN0001','RHN0002') and 
  ((TGLLPENCAIRAN BETWEEN '2019-05-01' AND '2019-05-12') or (TANGGAL_PERPANJANG like '%2019-05%'))
  /* tgl pencairan dari tanggal 1 mei 19 s/d 12 mei 19 ***/
