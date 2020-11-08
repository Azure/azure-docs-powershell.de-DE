---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 7EF20FC0-3E2A-4AFC-AC02-9B11C8952DB8
online version: ''
schema: 2.0.0
ms.openlocfilehash: 22263501f2a79a36c1ace1915ee6898c4833b52b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005769"
---
# <span data-ttu-id="08fb4-101">Get-AzureStorSimpleDeviceVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="08fb4-101">Get-AzureStorSimpleDeviceVolumeContainer</span></span>

## <span data-ttu-id="08fb4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="08fb4-102">SYNOPSIS</span></span>
<span data-ttu-id="08fb4-103">Ruft Volumen Container auf einem Gerät ab.</span><span class="sxs-lookup"><span data-stu-id="08fb4-103">Gets volume containers on a device.</span></span>

## <span data-ttu-id="08fb4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="08fb4-104">SYNTAX</span></span>

```
Get-AzureStorSimpleDeviceVolumeContainer -DeviceName <String> [-VolumeContainerName <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="08fb4-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="08fb4-105">DESCRIPTION</span></span>
<span data-ttu-id="08fb4-106">Das Cmdlet " **Get-AzureStorSimpleDeviceVolumeContainer** " Ruft eine Liste mit Volumen Containern auf einem Gerät oder einem Volumen Container mit dem angegebenen Namen ab.</span><span class="sxs-lookup"><span data-stu-id="08fb4-106">The **Get-AzureStorSimpleDeviceVolumeContainer** cmdlet gets a list of volume containers on a device, or volume container that has the specified name.</span></span>
<span data-ttu-id="08fb4-107">Das zurückgegebene Objekt enthält die folgenden Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="08fb4-107">The returned object contains the following properties:</span></span> 

- <span data-ttu-id="08fb4-108">**BandwidthRate**</span><span class="sxs-lookup"><span data-stu-id="08fb4-108">**BandwidthRate**</span></span>
- <span data-ttu-id="08fb4-109">**EncryptionKey**</span><span class="sxs-lookup"><span data-stu-id="08fb4-109">**EncryptionKey**</span></span>
- <span data-ttu-id="08fb4-110">**InstanceId**</span><span class="sxs-lookup"><span data-stu-id="08fb4-110">**InstanceId**</span></span>
- <span data-ttu-id="08fb4-111">**IsDefault**</span><span class="sxs-lookup"><span data-stu-id="08fb4-111">**IsDefault**</span></span>
- <span data-ttu-id="08fb4-112">**IsEncryptionEnabled**</span><span class="sxs-lookup"><span data-stu-id="08fb4-112">**IsEncryptionEnabled**</span></span>
- <span data-ttu-id="08fb4-113">**Namen**</span><span class="sxs-lookup"><span data-stu-id="08fb4-113">**Name**</span></span>
- <span data-ttu-id="08fb4-114">**OperationInProgress**</span><span class="sxs-lookup"><span data-stu-id="08fb4-114">**OperationInProgress**</span></span>
- <span data-ttu-id="08fb4-115">**Eigentum**</span><span class="sxs-lookup"><span data-stu-id="08fb4-115">**Owned**</span></span>
- <span data-ttu-id="08fb4-116">**PrimaryStorageAccountCredential**</span><span class="sxs-lookup"><span data-stu-id="08fb4-116">**PrimaryStorageAccountCredential**</span></span>
- <span data-ttu-id="08fb4-117">**SecretsEncryptionThumbprint**</span><span class="sxs-lookup"><span data-stu-id="08fb4-117">**SecretsEncryptionThumbprint**</span></span>
- <span data-ttu-id="08fb4-118">**VolumeCount**</span><span class="sxs-lookup"><span data-stu-id="08fb4-118">**VolumeCount**</span></span>

## <span data-ttu-id="08fb4-119">Beispiele</span><span class="sxs-lookup"><span data-stu-id="08fb4-119">EXAMPLES</span></span>

### <span data-ttu-id="08fb4-120">Beispiel 1: Abrufen aller Container auf einem Gerät</span><span class="sxs-lookup"><span data-stu-id="08fb4-120">Example 1: Get all the containers on a device</span></span>
```
PS C:\>Get-AzureStorSimpleDeviceVolumeContainer -DeviceName "8600-Bravo 001"
InstanceId                           Name                                             IsEncryptionEnabled  Owned BandwidthRate                                    PrimaryStorageAccountCredential                 VolumeCount                                    
----------                           ----                                             -------------------  ----- -------------                                    -------------------------------                 -----------                                    
127135b6-92de-4f53-850d-70e1f9a38cbe Test_Container                                   False                True  0                                                Test_Account                                    6
```

<span data-ttu-id="08fb4-121">Dieser Befehl ruft eine Liste der Volumen Container auf dem Gerät mit dem Namen 8600-Bravo 001 ab.</span><span class="sxs-lookup"><span data-stu-id="08fb4-121">This command gets a list of the volume containers on the device named 8600-Bravo 001.</span></span>

### <span data-ttu-id="08fb4-122">Beispiel 2: Abrufen eines Containers mit dem Namen</span><span class="sxs-lookup"><span data-stu-id="08fb4-122">Example 2: Get a container by using its name</span></span>
```
PS C:\>Get-AzureStorSimpleDeviceVolumeContainer -DeviceName "Contoso63-AppVm" -VolumeContainerName "Container08"
VERBOSE: ClientRequestId: 8027c66a-869b-4ea3-97a2-e17d98ec751c_PS
VERBOSE: ClientRequestId: 344f9be5-0887-4d37-98ef-e45c557774f1_PS
VERBOSE: ClientRequestId: 14919be5-d6f5-4f81-b7f1-d7fafff2238c_PS


BandwidthRate                   : 256
EncryptionKey                   : 
InstanceId                      : 04ea9aad-7a56-4a50-b195-86061b0a810a
IsDefault                       : False
IsEncryptionEnabled             : False
Name                            : Container03
OperationInProgress             : None
Owned                           : True
PrimaryStorageAccountCredential : Microsoft.WindowsAzure.Management.StorSimple.Models.StorageAccountCredentialResponse
SecretsEncryptionThumbprint     : 
VolumeCount                     : 5

VERBOSE: Volume container with name: Container03 is found.
```

<span data-ttu-id="08fb4-123">Dieser Befehl ruft den Volumen Container mit dem Namen Container08 auf dem Gerät mit dem Namen Contoso63-AppVm ab.</span><span class="sxs-lookup"><span data-stu-id="08fb4-123">This command gets the volume container named Container08 on the device named Contoso63-AppVm.</span></span>

## <span data-ttu-id="08fb4-124">Parameter</span><span class="sxs-lookup"><span data-stu-id="08fb4-124">PARAMETERS</span></span>

### <span data-ttu-id="08fb4-125">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="08fb4-125">-DeviceName</span></span>
<span data-ttu-id="08fb4-126">Gibt den Namen eines StorSimple-Geräts an.</span><span class="sxs-lookup"><span data-stu-id="08fb4-126">Specifies the name of a StorSimple device.</span></span>
<span data-ttu-id="08fb4-127">Dieses Cmdlet ruft Volumen Container vom Gerät ab, das dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="08fb4-127">This cmdlet gets volume containers from the device that this parameter specifies.</span></span>

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

### <span data-ttu-id="08fb4-128">-Profil</span><span class="sxs-lookup"><span data-stu-id="08fb4-128">-Profile</span></span>
<span data-ttu-id="08fb4-129">Gibt ein Azure-Profil an.</span><span class="sxs-lookup"><span data-stu-id="08fb4-129">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="08fb4-130">-VolumeContainerName</span><span class="sxs-lookup"><span data-stu-id="08fb4-130">-VolumeContainerName</span></span>
<span data-ttu-id="08fb4-131">Gibt den Namen des abzurufenden Volumen Containers an.</span><span class="sxs-lookup"><span data-stu-id="08fb4-131">Specifies the name of the volume container to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08fb4-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08fb4-132">CommonParameters</span></span>
<span data-ttu-id="08fb4-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08fb4-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08fb4-134">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="08fb4-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08fb4-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="08fb4-135">INPUTS</span></span>

### <span data-ttu-id="08fb4-136">Keine</span><span class="sxs-lookup"><span data-stu-id="08fb4-136">None</span></span>

## <span data-ttu-id="08fb4-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="08fb4-137">OUTPUTS</span></span>

### <span data-ttu-id="08fb4-138">DataContainer, IList\<DataContainer\></span><span class="sxs-lookup"><span data-stu-id="08fb4-138">DataContainer, IList\<DataContainer\></span></span>
<span data-ttu-id="08fb4-139">Wenn Sie den *VolumeContainerName* -Parameter angeben, gibt dieses Cmdlet ein **DataContainer** -Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="08fb4-139">This cmdlet returns a **DataContainer** object, if you specify the *VolumeContainerName* parameter.</span></span>
<span data-ttu-id="08fb4-140">Wenn Sie diesen Parameter nicht angeben, gibt dieses Cmdlet ein **IList \<DataContainer\>** -Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="08fb4-140">If you do not specify that parameter, this cmdlet returns an **IList\<DataContainer\>** object.</span></span>

## <span data-ttu-id="08fb4-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="08fb4-141">NOTES</span></span>

## <span data-ttu-id="08fb4-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="08fb4-142">RELATED LINKS</span></span>

[<span data-ttu-id="08fb4-143">Neu – AzureStorSimpleDeviceVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="08fb4-143">New-AzureStorSimpleDeviceVolumeContainer</span></span>](./New-AzureStorSimpleDeviceVolumeContainer.md)

[<span data-ttu-id="08fb4-144">Remove-AzureStorSimpleDeviceVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="08fb4-144">Remove-AzureStorSimpleDeviceVolumeContainer</span></span>](./Remove-AzureStorSimpleDeviceVolumeContainer.md)


