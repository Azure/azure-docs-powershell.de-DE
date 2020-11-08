---
external help file: ''
Module Name: Azs.Compute.Admin
online version: https://docs.microsoft.com/powershell/module/azs.compute.admin/get-azsdisk
schema: 2.0.0
ms.openlocfilehash: 9c3c87e7c62764cff0a7d6b9d65a3dfe3df31990
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94007281"
---
# <span data-ttu-id="4b194-101">Get-AzsDisk</span><span class="sxs-lookup"><span data-stu-id="4b194-101">Get-AzsDisk</span></span>

## <span data-ttu-id="4b194-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4b194-102">SYNOPSIS</span></span>
<span data-ttu-id="4b194-103">Gibt den Datenträger zurück.</span><span class="sxs-lookup"><span data-stu-id="4b194-103">Returns the disk.</span></span>

## <span data-ttu-id="4b194-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4b194-104">SYNTAX</span></span>

### <span data-ttu-id="4b194-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="4b194-105">List (Default)</span></span>
```
Get-AzsDisk [-Location <String>] [-SubscriptionId <String[]>] [-Count <Int32>] [-ScaleUnit <String>]
 [-SharePath <String>] [-Start <Int32>] [-Status <String>] [-UserSubscriptionId <String>]
 [-VolumeLabel <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="4b194-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="4b194-106">Get</span></span>
```
Get-AzsDisk -Name <String> [-Location <String>] [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="4b194-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="4b194-107">GetViaIdentity</span></span>
```
Get-AzsDisk -InputObject <IComputeAdminIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="4b194-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4b194-108">DESCRIPTION</span></span>
<span data-ttu-id="4b194-109">Gibt den Datenträger zurück.</span><span class="sxs-lookup"><span data-stu-id="4b194-109">Returns the disk.</span></span>

## <span data-ttu-id="4b194-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4b194-110">EXAMPLES</span></span>

### <span data-ttu-id="4b194-111">Beispiel 1: Abrufen aller Datenträger</span><span class="sxs-lookup"><span data-stu-id="4b194-111">Example 1: Get All Disks</span></span> 
```powershell
PS C:\> Get-AzsDisk
```

<span data-ttu-id="4b194-112">Ohne Parameter `Get-AzsDisk` werden alle Datenträger aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="4b194-112">Without any parameters, `Get-AzsDisk` will list all Disks.</span></span>

### <span data-ttu-id="4b194-113">Beispiel 2: Abrufen eines Datenträgers anhand des Namens</span><span class="sxs-lookup"><span data-stu-id="4b194-113">Example 2: Get a Disk by Name</span></span>
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

<span data-ttu-id="4b194-114">Geben Sie einen Datenträger `Name` an, um ihn abzurufen.</span><span class="sxs-lookup"><span data-stu-id="4b194-114">Specify a disk by its `Name` to retrieve it.</span></span>

### <span data-ttu-id="4b194-115">Beispiel 3: Abrufen einer angegebenen Anzahl von Datenträgern</span><span class="sxs-lookup"><span data-stu-id="4b194-115">Example 3: Get a Specified number of Disks</span></span>
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

<span data-ttu-id="4b194-116">Verwenden Sie den `Count` Parameter, um eine bestimmte Anzahl von Datenträgern abzurufen.</span><span class="sxs-lookup"><span data-stu-id="4b194-116">Use the `Count` parameter to retrieve a specific number of disks.</span></span>

### <span data-ttu-id="4b194-117">Beispiel 4: Abrufen aller Datenträger an einem bestimmten Speicherort</span><span class="sxs-lookup"><span data-stu-id="4b194-117">Example 4: Get all disks in specific location</span></span>
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

<span data-ttu-id="4b194-118">Verwenden des `ScaleUnit` or- `VolumeLabel` Parameters zum Auflisten aller Datenträger an einem bestimmten Speicherort</span><span class="sxs-lookup"><span data-stu-id="4b194-118">Use the `ScaleUnit` or `VolumeLabel` parameter to list all disks in specific location</span></span>

## <span data-ttu-id="4b194-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="4b194-119">PARAMETERS</span></span>

### <span data-ttu-id="4b194-120">-Anzahl</span><span class="sxs-lookup"><span data-stu-id="4b194-120">-Count</span></span>
<span data-ttu-id="4b194-121">Die maximale Anzahl von Datenträgern, die zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="4b194-121">The maximum number of disks to return.</span></span>

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

### <span data-ttu-id="4b194-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b194-122">-DefaultProfile</span></span>
<span data-ttu-id="4b194-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4b194-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4b194-124">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="4b194-124">-InputObject</span></span>
<span data-ttu-id="4b194-125">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="4b194-125">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="4b194-126">-Standort</span><span class="sxs-lookup"><span data-stu-id="4b194-126">-Location</span></span>
<span data-ttu-id="4b194-127">Der Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="4b194-127">Location of the resource.</span></span>

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

### <span data-ttu-id="4b194-128">-Name</span><span class="sxs-lookup"><span data-stu-id="4b194-128">-Name</span></span>
<span data-ttu-id="4b194-129">Die Datenträger-GUID als Identität.</span><span class="sxs-lookup"><span data-stu-id="4b194-129">The disk guid as identity.</span></span>

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

### <span data-ttu-id="4b194-130">-ScaleUnit</span><span class="sxs-lookup"><span data-stu-id="4b194-130">-ScaleUnit</span></span>
<span data-ttu-id="4b194-131">Die Skalierungseinheit, zu der die Ressource gehört.</span><span class="sxs-lookup"><span data-stu-id="4b194-131">The scale unit which the resource belongs to.</span></span>

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

### <span data-ttu-id="4b194-132">-SharePath</span><span class="sxs-lookup"><span data-stu-id="4b194-132">-SharePath</span></span>
<span data-ttu-id="4b194-133">Die Freigabe, zu der die Ressource gehört.</span><span class="sxs-lookup"><span data-stu-id="4b194-133">The share which the resource belongs to.</span></span>

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

### <span data-ttu-id="4b194-134">-Start</span><span class="sxs-lookup"><span data-stu-id="4b194-134">-Start</span></span>
<span data-ttu-id="4b194-135">Der startIndex von Datenträgern in Query.</span><span class="sxs-lookup"><span data-stu-id="4b194-135">The start index of disks in query.</span></span>

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

### <span data-ttu-id="4b194-136">-Status</span><span class="sxs-lookup"><span data-stu-id="4b194-136">-Status</span></span>
<span data-ttu-id="4b194-137">Die Parameter des Datenträger Zustands.</span><span class="sxs-lookup"><span data-stu-id="4b194-137">The parameters of disk state.</span></span>

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

### <span data-ttu-id="4b194-138">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="4b194-138">-SubscriptionId</span></span>
<span data-ttu-id="4b194-139">Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="4b194-139">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="4b194-140">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="4b194-140">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="4b194-141">-UserSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4b194-141">-UserSubscriptionId</span></span>
<span data-ttu-id="4b194-142">Benutzer-Abonnement-ID, zu der die Ressource gehört.</span><span class="sxs-lookup"><span data-stu-id="4b194-142">User Subscription Id which the resource belongs to.</span></span>

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

### <span data-ttu-id="4b194-143">-VolumeLabel</span><span class="sxs-lookup"><span data-stu-id="4b194-143">-VolumeLabel</span></span>
<span data-ttu-id="4b194-144">Die Datenträgerbeschriftung des Volumes, zu dem die Ressource gehört.</span><span class="sxs-lookup"><span data-stu-id="4b194-144">The volume label of the volume which the resource belongs to.</span></span>

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

### <span data-ttu-id="4b194-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b194-145">CommonParameters</span></span>
<span data-ttu-id="4b194-146">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b194-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b194-147">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4b194-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b194-148">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4b194-148">INPUTS</span></span>

### <span data-ttu-id="4b194-149">Microsoft. Azure. PowerShell. Cmdlets. ComputeAdmin. Models. IComputeAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="4b194-149">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.IComputeAdminIdentity</span></span>

## <span data-ttu-id="4b194-150">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4b194-150">OUTPUTS</span></span>

### <span data-ttu-id="4b194-151">Microsoft. Azure. PowerShell. Cmdlets. ComputeAdmin. Models. Api20180730Preview. iDisk</span><span class="sxs-lookup"><span data-stu-id="4b194-151">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20180730Preview.IDisk</span></span>



## <span data-ttu-id="4b194-152">Notizen</span><span class="sxs-lookup"><span data-stu-id="4b194-152">NOTES</span></span>

<span data-ttu-id="4b194-153">Komplexe Parametereigenschaften Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="4b194-153">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4b194-154">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="4b194-154">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="4b194-155">Inputobject <IComputeAdminIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="4b194-155">INPUTOBJECT <IComputeAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="4b194-156">`[DiskId <String>]`: Die Datenträger-GUID als Identität.</span><span class="sxs-lookup"><span data-stu-id="4b194-156">`[DiskId <String>]`: The disk guid as identity.</span></span>
  - <span data-ttu-id="4b194-157">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="4b194-157">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="4b194-158">`[Location <String>]`: Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="4b194-158">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="4b194-159">`[MigrationId <String>]`: Der GUID-Name des Migrationsauftrags.</span><span class="sxs-lookup"><span data-stu-id="4b194-159">`[MigrationId <String>]`: The migration job guid name.</span></span>
  - <span data-ttu-id="4b194-160">`[Offer <String>]`: Name des Angebots.</span><span class="sxs-lookup"><span data-stu-id="4b194-160">`[Offer <String>]`: Name of the offer.</span></span>
  - <span data-ttu-id="4b194-161">`[Publisher <String>]`: Name des Herausgebers.</span><span class="sxs-lookup"><span data-stu-id="4b194-161">`[Publisher <String>]`: Name of the publisher.</span></span>
  - <span data-ttu-id="4b194-162">`[QuotaName <String>]`: Name des Kontingents.</span><span class="sxs-lookup"><span data-stu-id="4b194-162">`[QuotaName <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="4b194-163">`[Sku <String>]`: Name der SKU.</span><span class="sxs-lookup"><span data-stu-id="4b194-163">`[Sku <String>]`: Name of the SKU.</span></span>
  - <span data-ttu-id="4b194-164">`[SubscriptionId <String>]`: Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="4b194-164">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="4b194-165">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="4b194-165">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="4b194-166">`[Type <String>]`: Typ der Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="4b194-166">`[Type <String>]`: Type of extension.</span></span>
  - <span data-ttu-id="4b194-167">`[Version <String>]`: Die Version der Ressource.</span><span class="sxs-lookup"><span data-stu-id="4b194-167">`[Version <String>]`: The version of the resource.</span></span>

## <span data-ttu-id="4b194-168">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4b194-168">RELATED LINKS</span></span>

