file(GLOB JPEG_SRCS LibJPEG/jaricom.c
					LibJPEG/jcapimin.c
					LibJPEG/jcapistd.c
					LibJPEG/jcarith.c
					LibJPEG/jccoefct.c
					LibJPEG/jccolor.c
					LibJPEG/jcdctmgr.c
					LibJPEG/jchuff.c
					LibJPEG/jcinit.c
					LibJPEG/jcmainct.c
					LibJPEG/jcmarker.c
					LibJPEG/jcmaster.c
					LibJPEG/jcomapi.c
					LibJPEG/jcparam.c
					LibJPEG/jcprepct.c
					LibJPEG/jcsample.c
					LibJPEG/jctrans.c
					LibJPEG/jdapimin.c
					LibJPEG/jdapistd.c
					LibJPEG/jdarith.c
					LibJPEG/jdatadst.c
					LibJPEG/jdatasrc.c
					LibJPEG/jdcoefct.c
					LibJPEG/jdcolor.c
					LibJPEG/jddctmgr.c
					LibJPEG/jdhuff.c
					LibJPEG/jdinput.c
					LibJPEG/jdmainct.c
					LibJPEG/jdmarker.c
					LibJPEG/jdmaster.c
					LibJPEG/jdmerge.c
					LibJPEG/jdpostct.c
					LibJPEG/jdsample.c
					LibJPEG/jdtrans.c
					LibJPEG/jerror.c
					LibJPEG/jfdctflt.c
					LibJPEG/jfdctfst.c
					LibJPEG/jfdctint.c
					LibJPEG/jidctflt.c
					LibJPEG/jidctfst.c
					LibJPEG/jidctint.c
					LibJPEG/jmemmgr.c
					LibJPEG/jmemnobs.c
					LibJPEG/jquant1.c
					LibJPEG/jquant2.c
					LibJPEG/jutils.c
					LibJPEG/transupp.c
					)

set(INCS ${CMAKE_CURRENT_SOURCE_DIR}/LibJPEG)
__add_real_target(LibJPEG lib SOURCE ${JPEG_SRCS}
							  DEF _CRT_SECURE_NO_DEPRECATE
							  INC ${INCS}
							  INTERFACE ${CMAKE_CURRENT_SOURCE_DIR}
							  ) 
							  
if(CC_INSTALL_OPENJPEG)
	__install_directory_specif(${CMAKE_CURRENT_SOURCE_DIR}/LibJPEG/ LibJPEG)
endif()