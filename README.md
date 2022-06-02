with open("inserir_script.txt", "r") as readFile:
    with open("coloque.txt", "a") as creatFile:
        for x in readFile:
            linha = x.split(' ')
            creatFile.write("\nINSERT INTO parametro_clinico (COD_PRM, DSC_PRM, COD_TIPO_PRM, TMN_PRM, TMN_DEC_PRM, "
                            "\nNUM_MAX_PRM, NUM_MIN_PRM, VISU_AFE_ANT, USA_TAG, SN_COMP_EXAME, "
                            "SN_MED_LAB, SN_PROTOCOLO, TP_CLASSIFICACAO,DS_APRESENTACAO, SN_ENCAMINHAMENTO, "
                            "SN_PARECER,\nSN_REP_DIAGNOSTICO, DS_SQL, SN_EDITA_DESC_BH, SN_AGRUPA_MED_BH) "
                            "VALUES ('" + linha[0] + "', '" + linha[1] + "','" + linha[2] + "', '" + linha[3] + "', "
                            "'0', '0', '0', 'Q', 'S', 'N', 'M', 'N', 'N','" + linha[1] + "', 'N', 'N', 'N', '<CLOB>', "
                            "'N', 'N'); ")
