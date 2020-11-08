---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: F16BCE0C-1F2C-4FB7-972D-28BE3CCD96D9
online version: ''
schema: 2.0.0
ms.openlocfilehash: dc41efa1901debf2efabf66f8d27f00da7eafe5f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005717"
---
# <span data-ttu-id="3cfde-101">New-AzureStorSimpleVirtualDevice</span><span class="sxs-lookup"><span data-stu-id="3cfde-101">New-AzureStorSimpleVirtualDevice</span></span>

## <span data-ttu-id="3cfde-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3cfde-102">SYNOPSIS</span></span>
<span data-ttu-id="3cfde-103">Erstellt ein virtuelles StorSimple-Gerät.</span><span class="sxs-lookup"><span data-stu-id="3cfde-103">Creates a virtual StorSimple device.</span></span>

## <span data-ttu-id="3cfde-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3cfde-104">SYNTAX</span></span>

### <span data-ttu-id="3cfde-105">CreateNewStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3cfde-105">CreateNewStorageAccount</span></span>
```
New-AzureStorSimpleVirtualDevice -VirtualDeviceName <String> -VirtualNetworkName <String> -SubNetName <String>
 [-StorageAccountName <String>] [-CreateNewStorageAccount] [-PersistAzureVMOnFailrue]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="3cfde-106">UseExistingStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3cfde-106">UseExistingStorageAccount</span></span>
```
New-AzureStorSimpleVirtualDevice -VirtualDeviceName <String> -VirtualNetworkName <String> -SubNetName <String>
 -StorageAccountName <String> [-PersistAzureVMOnFailrue] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="3cfde-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3cfde-107">DESCRIPTION</span></span>
<span data-ttu-id="3cfde-108">Mit dem Cmdlet **New-AzureStorSimpleVirtualDevice** wird ein virtuelles StorSimple-Gerät erstellt.</span><span class="sxs-lookup"><span data-stu-id="3cfde-108">The **New-AzureStorSimpleVirtualDevice** cmdlet creates a virtual StorSimple device.</span></span>
<span data-ttu-id="3cfde-109">Geben Sie einen Gerätenamen für das Gerät an.</span><span class="sxs-lookup"><span data-stu-id="3cfde-109">Specify a device name for the device.</span></span>
<span data-ttu-id="3cfde-110">Geben Sie die Details für virtuelles Netzwerk und Subnetz für das virtuelle Netzwerk im gleichen Abonnement an.</span><span class="sxs-lookup"><span data-stu-id="3cfde-110">Specify virtual network and subnet details for the virtual network in the same subscription.</span></span>
<span data-ttu-id="3cfde-111">Der Geo sollte mit dem Geo übereinstimmen, in dem die StorSimple-Ressource erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="3cfde-111">The geo should match the geo in which the StorSimple resource is created.</span></span>
<span data-ttu-id="3cfde-112">Wenn Sie ein vorhandenes Speicherkonto für dieses virtuelle Gerät verwenden möchten, geben Sie den Namen an.</span><span class="sxs-lookup"><span data-stu-id="3cfde-112">To use an existing storage account for this virtual device, specify the name.</span></span>
<span data-ttu-id="3cfde-113">Wenn Sie ein neues Speicherkonto für dieses virtuelle Gerät erstellen möchten, geben Sie den Parameter *StorageAccountName* und *CreateNewStorageAccount* an.</span><span class="sxs-lookup"><span data-stu-id="3cfde-113">To create a new storage account for this virtual device, specify both the *StorageAccountName* and the *CreateNewStorageAccount* parameters.</span></span>

## <span data-ttu-id="3cfde-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3cfde-114">EXAMPLES</span></span>

### <span data-ttu-id="3cfde-115">Beispiel 1: Erstellen eines virtuellen Geräts mit einem neuen Konto und einem vorhandenen Netzwerk</span><span class="sxs-lookup"><span data-stu-id="3cfde-115">Example 1: Create a virtual device with a new account and an existing network</span></span>
```
PS C:\>New-AzureStorSimpleVirtualDevice -VirtualDeviceName "Contosodevice02" -VirtualNetworkName "Saas2vpn" -SubNetName "TenantSubnet" -StorageAccountName "AzureTenant04" -CreateNewStorageAccount
64e4c564-b0ac-44b0-afb4-adf28ac24ad0
VERBOSE: The create job is triggered successfully. Please use the command Get-AzureStorSimpleJob -InstanceId 64e4c564-b0ac-44b0-afb4-adf28ac24ad0 for tracking the job's status
```

<span data-ttu-id="3cfde-116">Mit diesem Befehl wird ein virtuelles Gerät erstellt, das ein neues Speicherkonto und ein vorhandenes virtuelles Netzwerk verwendet.</span><span class="sxs-lookup"><span data-stu-id="3cfde-116">This command creates a virtual device that uses a new storage account and an existing virtual network.</span></span>

### <span data-ttu-id="3cfde-117">Beispiel 2: Erstellen eines virtuellen Geräts mit einem vorhandenen Konto und einem virtuellen Netzwerk</span><span class="sxs-lookup"><span data-stu-id="3cfde-117">Example 2: Create a virtual device with an existing account and virtual network</span></span>
```
PS C:\>New-AzureStorSimpleVirtualDevice -VirtualDeviceName "ContosoDevice07" -VirtualNetworkName "Saas2vpn" -SubNetName TenantSubnet -StorageAccountName azurecisbvtdnd
2a18a3b7-1ec6-481d-b95d-66ba8f67ceaf
VERBOSE: The create job is triggered successfully. Please use the command Get-AzureStorSimpleJob -InstanceId 2a18a3b7-1ec6-481d-b95d-66ba8f67ceaf for tracking the job's status
```

<span data-ttu-id="3cfde-118">Mit diesem Befehl wird ein virtuelles Gerät erstellt, das ein vorhandenes Speicherkonto und ein vorhandenes virtuelles Netzwerk verwendet.</span><span class="sxs-lookup"><span data-stu-id="3cfde-118">This command creates a virtual device that uses an existing storage account and an existing virtual network.</span></span>

## <span data-ttu-id="3cfde-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="3cfde-119">PARAMETERS</span></span>

### <span data-ttu-id="3cfde-120">-CreateNewStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3cfde-120">-CreateNewStorageAccount</span></span>
<span data-ttu-id="3cfde-121">Gibt an, dass dieses Cmdlet ein neues Speicherkonto erstellt.</span><span class="sxs-lookup"><span data-stu-id="3cfde-121">Indicates that this cmdlet creates a new storage account.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: CreateNewStorageAccount
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cfde-122">-PersistAzureVMOnFailrue</span><span class="sxs-lookup"><span data-stu-id="3cfde-122">-PersistAzureVMOnFailrue</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cfde-123">-Profil</span><span class="sxs-lookup"><span data-stu-id="3cfde-123">-Profile</span></span>
<span data-ttu-id="3cfde-124">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="3cfde-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="3cfde-125">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="3cfde-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cfde-126">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="3cfde-126">-StorageAccountName</span></span>
<span data-ttu-id="3cfde-127">Gibt den Namen eines speicherkontos an.</span><span class="sxs-lookup"><span data-stu-id="3cfde-127">Specifies the name of a storage account.</span></span>

```yaml
Type: String
Parameter Sets: CreateNewStorageAccount
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: UseExistingStorageAccount
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cfde-128">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="3cfde-128">-SubNetName</span></span>
<span data-ttu-id="3cfde-129">Gibt den Namen eines virtuellen Subnetzes an.</span><span class="sxs-lookup"><span data-stu-id="3cfde-129">Specifies the name of a virtual subnet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cfde-130">-VirtualDeviceName</span><span class="sxs-lookup"><span data-stu-id="3cfde-130">-VirtualDeviceName</span></span>
<span data-ttu-id="3cfde-131">Gibt einen Namen für das virtuelle Gerät an.</span><span class="sxs-lookup"><span data-stu-id="3cfde-131">Specifies a name for the virtual device.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cfde-132">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="3cfde-132">-VirtualNetworkName</span></span>
<span data-ttu-id="3cfde-133">Gibt den Namen eines virtuellen Netzwerks an.</span><span class="sxs-lookup"><span data-stu-id="3cfde-133">Specifies the name of a virtual network.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: VNetName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cfde-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3cfde-134">CommonParameters</span></span>
<span data-ttu-id="3cfde-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3cfde-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3cfde-136">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3cfde-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3cfde-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3cfde-137">INPUTS</span></span>

## <span data-ttu-id="3cfde-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3cfde-138">OUTPUTS</span></span>

### <span data-ttu-id="3cfde-139">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="3cfde-139">String</span></span>
<span data-ttu-id="3cfde-140">Dieses Cmdlet gibt die ID des Auftrags zurück, der das virtuelle Gerät erstellt.</span><span class="sxs-lookup"><span data-stu-id="3cfde-140">This cmdlet returns the ID of the job that creates the virtual device.</span></span>
<span data-ttu-id="3cfde-141">Sie können diese ID verwenden, um den Fortschritt mithilfe des Get-AzureStorSimpleJob-Cmdlets zu verfolgen.</span><span class="sxs-lookup"><span data-stu-id="3cfde-141">You can use this ID to track the progress using the Get-AzureStorSimpleJob cmdlet.</span></span>

## <span data-ttu-id="3cfde-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="3cfde-142">NOTES</span></span>

## <span data-ttu-id="3cfde-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3cfde-143">RELATED LINKS</span></span>

[<span data-ttu-id="3cfde-144">Get-AzureStorSimpleJob</span><span class="sxs-lookup"><span data-stu-id="3cfde-144">Get-AzureStorSimpleJob</span></span>](./Get-AzureStorSimpleJob.md)

[<span data-ttu-id="3cfde-145">Satz-AzureStorSimpleVirtualDevice</span><span class="sxs-lookup"><span data-stu-id="3cfde-145">Set-AzureStorSimpleVirtualDevice</span></span>](./Set-AzureStorSimpleVirtualDevice.md)


