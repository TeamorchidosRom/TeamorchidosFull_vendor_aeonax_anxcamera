# TeamorchidosRom
Modified Camera example how to add to rom

added to device example target phone twolip

cd device/xiaomi/twolip

then

nano BoardConfig.mk add (near start) -include vendor/aeonax/ANXCamera/BoardConfigAnx.mk

then

nano device.mk add (near end) $(call inherit-product-if-exists, vendor/aeonax/ANXCamera/anx-vendor.mk)

if not already in your manifest

add like this at top of tree

git clone https://github.com/TeamorchidosRom/TeamorchidosFull_vendor_aeonax_anxcamera vendor/aeonax/ANXCamera

Note this was removed from

vendor/aeonax/ANXCamera/proprietary/system/lib64/

removed files that are duplicated rm -rf libcamera2ndk.so rm -rf libcamera_client.so rm -rf libcamera_metadata.so rm -rf libheif.so rm -rf libjni_pacprocessor.so
