---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 9436E1AB-870F-4717-ABE0-55A90C07F7E4
online version: ''
schema: 2.0.0
ms.openlocfilehash: 555ce014bbbf7174b3f7142cf7e2f217317eadc6
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006497"
---
# <span data-ttu-id="3005f-101">Get-AzureStorSimpleDeviceConnectedInitiator</span><span class="sxs-lookup"><span data-stu-id="3005f-101">Get-AzureStorSimpleDeviceConnectedInitiator</span></span>

## <span data-ttu-id="3005f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3005f-102">SYNOPSIS</span></span>
<span data-ttu-id="3005f-103">Ruft die iSCSI-Verbindungen ab, die für ein StorSimple-Gerät verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="3005f-103">Gets the iSCSI connections available for a StorSimple device.</span></span>

## <span data-ttu-id="3005f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3005f-104">SYNTAX</span></span>

### <span data-ttu-id="3005f-105">IdentifyById</span><span class="sxs-lookup"><span data-stu-id="3005f-105">IdentifyById</span></span>
```
Get-AzureStorSimpleDeviceConnectedInitiator -DeviceId <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="3005f-106">IdentifyByName</span><span class="sxs-lookup"><span data-stu-id="3005f-106">IdentifyByName</span></span>
```
Get-AzureStorSimpleDeviceConnectedInitiator -DeviceName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="3005f-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3005f-107">DESCRIPTION</span></span>
<span data-ttu-id="3005f-108">Das Cmdlet " **Get-AzureStorSimpleDeviceConnectedInitiator** " Ruft eine Liste der iSCSI-Verbindungen ab, die für ein StorSimple-Gerät verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="3005f-108">The **Get-AzureStorSimpleDeviceConnectedInitiator** cmdlet gets a list of the iSCSI connections available for a StorSimple device.</span></span>
<span data-ttu-id="3005f-109">Die von diesem Cmdlet zurückgegebenen iSCSI-Verbindungsobjekte enthalten die folgenden Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="3005f-109">The iSCSI connection objects that this cmdlet returns contain the following properties:</span></span>

- <span data-ttu-id="3005f-110">**AcrInstanceId**</span><span class="sxs-lookup"><span data-stu-id="3005f-110">**AcrInstanceId**</span></span>
- <span data-ttu-id="3005f-111">**AcrName**</span><span class="sxs-lookup"><span data-stu-id="3005f-111">**AcrName**</span></span>
- <span data-ttu-id="3005f-112">**AllowedVolumeNames**</span><span class="sxs-lookup"><span data-stu-id="3005f-112">**AllowedVolumeNames**</span></span>
- <span data-ttu-id="3005f-113">**InitiatorAddress**</span><span class="sxs-lookup"><span data-stu-id="3005f-113">**InitiatorAddress**</span></span>
- <span data-ttu-id="3005f-114">**Schnittstellen**</span><span class="sxs-lookup"><span data-stu-id="3005f-114">**Interfaces**</span></span>
- <span data-ttu-id="3005f-115">**IQN**</span><span class="sxs-lookup"><span data-stu-id="3005f-115">**Iqn**</span></span>
- <span data-ttu-id="3005f-116">**IscsiConnectionId**</span><span class="sxs-lookup"><span data-stu-id="3005f-116">**IscsiConnectionId**</span></span>

<span data-ttu-id="3005f-117">Dieses Cmdlet ruft nur dann Connection-Objekt ab, wenn iSCSI-Verbindungen für das Gerät aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="3005f-117">This cmdlet gets connection object only if iSCSI connections are turned on for the device.</span></span>
<span data-ttu-id="3005f-118">Standardmäßig sind Verbindungen deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="3005f-118">By default, connections are turned off.</span></span>

## <span data-ttu-id="3005f-119">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3005f-119">EXAMPLES</span></span>

### <span data-ttu-id="3005f-120">Beispiel 1: Abrufen aller Verbindungen für ein Gerät</span><span class="sxs-lookup"><span data-stu-id="3005f-120">Example 1: Get all connections for a device</span></span>
```
PS C:\>Get-AzureStorSimpleDeviceConnectedInitiator -DeviceName "Contoso63-AppVm"
VERBOSE: ClientRequestId: bec615b9-79ab-4671-88b0-287adeb6bf68_PS
VERBOSE: ClientRequestId: ef976c58-2660-41c8-aa15-c84e70c9d01c_PS
VERBOSE: ClientRequestId: 9b306b96-8e76-47ed-beda-d3bd2fb2bb82_PS
VERBOSE: ClientRequestId: 0f4fc743-0b60-45da-a45a-27f4b0f32bd2_PS

AcrInstanceId      : 55f24643-ab3a-4098-ade2-aa2b1a3ab18c
AcrName            : Contoso63-AppVm
AllowedVolumeNames : {Policyvolume1_Default}
InitiatorAddress   : 
Interfaces         : {Data0}
Iqn                : iqn10
IscsiConnectionId  : cfc144cb-00f1-44b1-9655-80b431f2161b

VERBOSE: 1 Iscsi Connection found!
```

<span data-ttu-id="3005f-121">Dieser Befehl ruft alle iSCSI-Verbindungen für das Gerät mit dem Namen Contoso63-AppVm.</span><span class="sxs-lookup"><span data-stu-id="3005f-121">This command gets all iSCSI connections for the device named Contoso63-AppVm.</span></span>
<span data-ttu-id="3005f-122">Dieser Befehl gibt nur dann Verbindungen zurück, wenn Verbindungen für das Gerät aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="3005f-122">This command returns connections only if connections are turned on for the device.</span></span>

## <span data-ttu-id="3005f-123">Parameter</span><span class="sxs-lookup"><span data-stu-id="3005f-123">PARAMETERS</span></span>

### <span data-ttu-id="3005f-124">-Geräte-Nr</span><span class="sxs-lookup"><span data-stu-id="3005f-124">-DeviceId</span></span>
<span data-ttu-id="3005f-125">Gibt die Instanz-ID des StorSimple-Geräts an, aus dem iSCSI-Initiatoren abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="3005f-125">Specifies the instance ID of the StorSimple device from which to get iSCSI initiators.</span></span>

```yaml
Type: String
Parameter Sets: IdentifyById
Aliases: ID

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3005f-126">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="3005f-126">-DeviceName</span></span>
<span data-ttu-id="3005f-127">Gibt den Namen des StorSimple-Geräts an, aus dem iSCSI-Initiatoren abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="3005f-127">Specifies the name of the StorSimple device from which to get iSCSI initiators.</span></span>

```yaml
Type: String
Parameter Sets: IdentifyByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3005f-128">-Profil</span><span class="sxs-lookup"><span data-stu-id="3005f-128">-Profile</span></span>
<span data-ttu-id="3005f-129">Gibt ein Azure-Profil an.</span><span class="sxs-lookup"><span data-stu-id="3005f-129">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="3005f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3005f-130">CommonParameters</span></span>
<span data-ttu-id="3005f-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3005f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3005f-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3005f-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3005f-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3005f-133">INPUTS</span></span>

### <span data-ttu-id="3005f-134">Keine</span><span class="sxs-lookup"><span data-stu-id="3005f-134">None</span></span>

## <span data-ttu-id="3005f-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3005f-135">OUTPUTS</span></span>

### <span data-ttu-id="3005f-136">Liste\<IscsiConnection\></span><span class="sxs-lookup"><span data-stu-id="3005f-136">List\<IscsiConnection\></span></span>
<span data-ttu-id="3005f-137">Dieses Cmdlet gibt ein iSCSI-Verbindungsobjekt zurück, das die folgenden Eigenschaften enthält:</span><span class="sxs-lookup"><span data-stu-id="3005f-137">This cmdlet returns an iSCSI connection object that contains the following properties:</span></span> 

- <span data-ttu-id="3005f-138">**AcrInstanceId**</span><span class="sxs-lookup"><span data-stu-id="3005f-138">**AcrInstanceId**</span></span>
- <span data-ttu-id="3005f-139">**AcrName**</span><span class="sxs-lookup"><span data-stu-id="3005f-139">**AcrName**</span></span>
- <span data-ttu-id="3005f-140">**AllowedVolumeNames**</span><span class="sxs-lookup"><span data-stu-id="3005f-140">**AllowedVolumeNames**</span></span>
- <span data-ttu-id="3005f-141">**InitiatorAddress**</span><span class="sxs-lookup"><span data-stu-id="3005f-141">**InitiatorAddress**</span></span>
- <span data-ttu-id="3005f-142">**Schnittstellen**</span><span class="sxs-lookup"><span data-stu-id="3005f-142">**Interfaces**</span></span>
- <span data-ttu-id="3005f-143">**IQN**</span><span class="sxs-lookup"><span data-stu-id="3005f-143">**Iqn**</span></span>
- <span data-ttu-id="3005f-144">**IscsiConnectionId**</span><span class="sxs-lookup"><span data-stu-id="3005f-144">**IscsiConnectionId**</span></span>

## <span data-ttu-id="3005f-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="3005f-145">NOTES</span></span>

## <span data-ttu-id="3005f-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3005f-146">RELATED LINKS</span></span>

[<span data-ttu-id="3005f-147">Get-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="3005f-147">Get-AzureStorSimpleAccessControlRecord</span></span>](./Get-AzureStorSimpleAccessControlRecord.md)


