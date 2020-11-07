---
external help file: ''
Module Name: Azs.Compute.Admin
online version: https://docs.microsoft.com/powershell/module/azs.compute.admin/get-azsdisk
schema: 2.0.0
ms.openlocfilehash: 9c3c87e7c62764cff0a7d6b9d65a3dfe3df31990
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844888"
---
# Get-AzsDisk

## Synopsis
Gibt den Datenträger zurück.

## Syntax

### Liste (Standard)
```
Get-AzsDisk [-Location <String>] [-SubscriptionId <String[]>] [-Count <Int32>] [-ScaleUnit <String>]
 [-SharePath <String>] [-Start <Int32>] [-Status <String>] [-UserSubscriptionId <String>]
 [-VolumeLabel <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### Erhalten
```
Get-AzsDisk -Name <String> [-Location <String>] [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### GetViaIdentity
```
Get-AzsDisk -InputObject <IComputeAdminIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## Beschreibung
Gibt den Datenträger zurück.

## Beispiele

### Beispiel 1: Abrufen aller Datenträger 
```powershell
PS C:\> Get-AzsDisk
```

Ohne Parameter `Get-AzsDisk` werden alle Datenträger aufgelistet.

### Beispiel 2: Abrufen eines Datenträgers anhand des Namens
```powershell
PS C:\> Get-AzsDisk -Name "426b8945-8a24-42ad-acdc-c26f16202489"

ActualSizeGb    : 24
DiskId          : 426b8945-8a24-42ad-acdc-c26f16202489
DiskSku         : Premium_LRS
DiskType        : Disk
Id              : /subscriptions/74c72bdc-d917-431c-a377-8ca80f4238a0/providers/Microsoft.Compute.Admin/locations/north
                  west/disks/426b8945-8a24-42ad-acdc-c26f16202489
Location        : northwest
ManagedBy       :
Name            : northwest/426b8945-8a24-42ad-acdc-c26f16202489
ProvisionSizeGb : 127
SharePath       : \\SU1FileServer.azs-long02-int.selfhost.corp.microsoft.com\SU1_ObjStore_3
Status          : Unattached
Type            : Microsoft.Compute.Admin/locations/disks
UserResourceId  : /subscriptions/74c72bdc-d917-431c-a377-8ca80f4238a0/resourceGroups/LADTEST/providers/Microsoft.Comput
                  e/Disks/TEST_OsDisk_1_426b89458a2442adacdcc26f16202489
```

Geben Sie einen Datenträger `Name` an, um ihn abzurufen.

### Beispiel 3: Abrufen einer angegebenen Anzahl von Datenträgern
```powershell
PS C:\>  Get-AzsDisk -Count 3

ActualSizeGb    : 24
DiskId          : 20f1619e-4210-47f6-81e6-b89e3028df06
DiskSku         : Premium_LRS
DiskType        : Disk
Id              : /subscriptions/74c72bdc-d917-431c-a377-8ca80f4238a0/providers/Microsoft.Compute.Admin/locations/north
                  west/disks/20f1619e-4210-47f6-81e6-b89e3028df06
Location        : northwest
ManagedBy       :
Name            : northwest/20f1619e-4210-47f6-81e6-b89e3028df06
ProvisionSizeGb : 127
SharePath       : \\SU1FileServer.azs-long02-int.selfhost.corp.microsoft.com\SU1_ObjStore_4
Status          : Unattached
Type            : Microsoft.Compute.Admin/locations/disks
UserResourceId  : /subscriptions/74c72bdc-d917-431c-a377-8ca80f4238a0/resourceGroups/RG1/providers/Microsoft.Compute/Di
                  sks/TEST_OsDisk_1_20f1619e421047f681e6b89e3028df06

ActualSizeGb    : 24
DiskId          : 38a767e4-4ceb-49fb-a53c-48de9b08aaae
DiskSku         : Standard_LRS
DiskType        : Disk
Id              : /subscriptions/74c72bdc-d917-431c-a377-8ca80f4238a0/providers/Microsoft.Compute.Admin/locations/north
                  west/disks/38a767e4-4ceb-49fb-a53c-48de9b08aaae
Location        : northwest
ManagedBy       :
Name            : northwest/38a767e4-4ceb-49fb-a53c-48de9b08aaae
ProvisionSizeGb : 127
SharePath       : \\SU1FileServer.azs-long02-int.selfhost.corp.microsoft.com\SU1_ObjStore_4
Status          : Unattached
Type            : Microsoft.Compute.Admin/locations/disks
UserResourceId  : /subscriptions/74c72bdc-d917-431c-a377-8ca80f4238a0/resourceGroups/SCTE/providers/Microsoft.Compute/D
                  isks/SCTETest_OsDisk_1_38a767e44ceb49fba53c48de9b08aaae

ActualSizeGb    : 24
DiskId          : 426b8945-8a24-42ad-acdc-c26f16202489
DiskSku         : Premium_LRS
DiskType        : Disk
Id              : /subscriptions/74c72bdc-d917-431c-a377-8ca80f4238a0/providers/Microsoft.Compute.Admin/locations/north
                  west/disks/426b8945-8a24-42ad-acdc-c26f16202489
Location        : northwest
ManagedBy       :
Name            : northwest/426b8945-8a24-42ad-acdc-c26f16202489
ProvisionSizeGb : 127
SharePath       : \\SU1FileServer.azs-long02-int.selfhost.corp.microsoft.com\SU1_ObjStore_3
Status          : Unattached
Type            : Microsoft.Compute.Admin/locations/disks
UserResourceId  : /subscriptions/74c72bdc-d917-431c-a377-8ca80f4238a0/resourceGroups/LADTEST/providers/Microsoft.Comput
                  e/Disks/TEST_OsDisk_1_426b89458a2442adacdcc26f16202489
```

Verwenden Sie den `Count` Parameter, um eine bestimmte Anzahl von Datenträgern abzurufen.

### Beispiel 4: Abrufen aller Datenträger an einem bestimmten Speicherort
```powershell
PS C:\> Get-AzsDisk -Status All -ScaleUnit s-cluster -VolumeLabel Objstore_4

ActualSizeGb    : 2
DiskId          : e4732f76-0753-40ec-80f5-8effdd0b437d
DiskSku         : Premium_LRS
DiskType        : Disk
Id              : /subscriptions/7829c784-cd3f-464a-b195-3be83c964c9c/providers/Microsoft.Compute.Admin/locations/redmond/disks/e4732f76-0753-40ec-80f5-8effdd0b437d
Location        : redmond
ManagedBy       : /subscriptions/7829c784-cd3f-464a-b195-3be83c964c9c/resourceGroups/rbactest/providers/Microsoft.Compute/virtualMachines/test1
Name            : redmond/e4732f76-0753-40ec-80f5-8effdd0b437d
ProvisionSizeGb : 30
SharePath       : \\SU1FileServer.s11r0401.masd.stbtest.microsoft.com\SU1_ObjStore_4
Status          : Reserved
Type            : Microsoft.Compute.Admin/locations/disks
UserResourceId  : /subscriptions/7829c784-cd3f-464a-b195-3be83c964c9c/resourceGroups/RBACTEST/providers/Microsoft.Compute/Disks/test1_OsDisk_1_e4732f76075340ec80f58effdd0b437d

ActualSizeGb    : 1
DiskId          : 0485cbc9-1efa-43bd-86c2-0e201d79c528
DiskSku         : Premium_LRS
DiskType        : Disk
Id              : /subscriptions/7829c784-cd3f-464a-b195-3be83c964c9c/providers/Microsoft.Compute.Admin/locations/redmond/disks/0485cbc9-1efa-43bd-86c2-0e201d79c528
Location        : redmond
ManagedBy       : /subscriptions/7829c784-cd3f-464a-b195-3be83c964c9c/resourceGroups/rbactest/providers/Microsoft.Compute/virtualMachines/test1
Name            : redmond/0485cbc9-1efa-43bd-86c2-0e201d79c528
ProvisionSizeGb : 64
SharePath       : \\SU1FileServer.s11r0401.masd.stbtest.microsoft.com\SU1_ObjStore_4
Status          : Reserved
Type            : Microsoft.Compute.Admin/locations/disks
UserResourceId  : /subscriptions/7829c784-cd3f-464a-b195-3be83c964c9c/resourceGroups/TESTRG1/providers/Microsoft.Compute/Disks/gpsdisk

ActualSizeGb    : 1
DiskId          : 137893db-e7ce-4907-a488-b35c5e928614
DiskSku         : Premium_LRS
DiskType        : Disk
Id              : /subscriptions/7829c784-cd3f-464a-b195-3be83c964c9c/providers/Microsoft.Compute.Admin/locations/redmond/disks/137893db-e7ce-4907-a488-b35c5e928614
Location        : redmond
ManagedBy       : /subscriptions/7829c784-cd3f-464a-b195-3be83c964c9c/resourceGroups/rbactest/providers/Microsoft.Compute/virtualMachines/test1
Name            : redmond/137893db-e7ce-4907-a488-b35c5e928614
ProvisionSizeGb : 55
SharePath       : \\SU1FileServer.s11r0401.masd.stbtest.microsoft.com\SU1_ObjStore_4
Status          : Reserved
Type            : Microsoft.Compute.Admin/locations/disks
UserResourceId  : /subscriptions/7829c784-cd3f-464a-b195-3be83c964c9c/resourceGroups/RBACTEST/providers/Microsoft.Compute/Disks/testdd
```

Verwenden des `ScaleUnit` or- `VolumeLabel` Parameters zum Auflisten aller Datenträger an einem bestimmten Speicherort

## Parameter

### -Anzahl
Die maximale Anzahl von Datenträgern, die zurückgegeben werden sollen.

```yaml
Type: System.Int32
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -Inputobject
Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.IComputeAdminIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### -Standort
Der Speicherort der Ressource.

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### -Name
Die Datenträger-GUID als Identität.

```yaml
Type: System.String
Parameter Sets: Get
Aliases: DiskId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -ScaleUnit
Die Skalierungseinheit, zu der die Ressource gehört.

```yaml
Type: System.String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -SharePath
Die Freigabe, zu der die Ressource gehört.

```yaml
Type: System.String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -Start
Der startIndex von Datenträgern in Query.

```yaml
Type: System.Int32
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -Status
Die Parameter des Datenträger Zustands.

```yaml
Type: System.String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -Abonnement-Nr
Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.
Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### -UserSubscriptionId
Benutzer-Abonnement-ID, zu der die Ressource gehört.

```yaml
Type: System.String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -VolumeLabel
Die Datenträgerbeschriftung des Volumes, zu dem die Ressource gehört.

```yaml
Type: System.String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## Eingaben

### Microsoft. Azure. PowerShell. Cmdlets. ComputeAdmin. Models. IComputeAdminIdentity

## Ausgaben

### Microsoft. Azure. PowerShell. Cmdlets. ComputeAdmin. Models. Api20180730Preview. iDisk



## Notizen

Komplexe Parametereigenschaften Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften. Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.

Inputobject <IComputeAdminIdentity> : Identity-Parameter
  - `[DiskId <String>]`: Die Datenträger-GUID als Identität.
  - `[Id <String>]`: Ressourcen Identitäts Pfad
  - `[Location <String>]`: Speicherort der Ressource.
  - `[MigrationId <String>]`: Der GUID-Name des Migrationsauftrags.
  - `[Offer <String>]`: Name des Angebots.
  - `[Publisher <String>]`: Name des Herausgebers.
  - `[QuotaName <String>]`: Name des Kontingents.
  - `[Sku <String>]`: Name der SKU.
  - `[SubscriptionId <String>]`: Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren. Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.
  - `[Type <String>]`: Typ der Erweiterung.
  - `[Version <String>]`: Die Version der Ressource.

## Verwandte Links

