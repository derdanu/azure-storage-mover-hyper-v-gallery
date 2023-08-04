# azure-storage-mover-hyper-v-gallery
Hyper-V Gallery for Azure Storage Mover Agent

# Setup Hyper-V Gallery
The following commands must be executed on Administrator PowerShell.

## Add gallery
    New-ItemProperty -Path "HKLM:\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Virtualization\"  `
        -Name 'GalleryLocations' -PropertyType MultiString -Value (
        'https://raw.githubusercontent.com/derdanu/azure-storage-mover-hyper-v-gallery/main/image.json',
        'https://go.microsoft.com/fwlink/?linkid=851584'
        )


## Remove gallery
    Remove-ItemProperty -Path "HKLM:\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Virtualization\" -Name "GalleryLocations"

