---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 71302FB6-7E2B-4972-A743-AB537AC7CD79
online version: ''
schema: 2.0.0
ms.openlocfilehash: 79e194e0f8dda4392dec191881702c680bf172ac
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006758"
---
# <span data-ttu-id="edaee-101">Get-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="edaee-101">Get-AzureStorSimpleAccessControlRecord</span></span>

## <span data-ttu-id="edaee-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="edaee-102">SYNOPSIS</span></span>
<span data-ttu-id="edaee-103">Ruft Zugriffssteuerungseinträge in einer Dienstkonfiguration ab.</span><span class="sxs-lookup"><span data-stu-id="edaee-103">Gets access control records in a service configuration.</span></span>

## <span data-ttu-id="edaee-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="edaee-104">SYNTAX</span></span>

```
Get-AzureStorSimpleAccessControlRecord [-ACRName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="edaee-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="edaee-105">DESCRIPTION</span></span>
<span data-ttu-id="edaee-106">Das Cmdlet " **Get-AzureStorSimpleAccessControlRecord** " ruft Zugriffssteuerungseinträge in der StorSimple-Manager-Dienstkonfiguration ab.</span><span class="sxs-lookup"><span data-stu-id="edaee-106">The **Get-AzureStorSimpleAccessControlRecord** cmdlet gets access control records in the StorSimple Manager service configuration.</span></span>
<span data-ttu-id="edaee-107">Mit diesem Cmdlet werden alle Datensätze oder ein benannter Datensatz abgerufen.</span><span class="sxs-lookup"><span data-stu-id="edaee-107">This cmdlet gets all records or a named record.</span></span>

<span data-ttu-id="edaee-108">Zugriffssteuerungseinträge sind Container mit iSCSI-initiatorparameter.</span><span class="sxs-lookup"><span data-stu-id="edaee-108">Access control records are containers of iSCSI initiator parameters.</span></span>
<span data-ttu-id="edaee-109">Diese Parameter geben an, welche Initiatoren auf ein Volume zugreifen können.</span><span class="sxs-lookup"><span data-stu-id="edaee-109">These parameters specify which initiators can access a volume.</span></span>
<span data-ttu-id="edaee-110">Wenn ein iSCSI-Initiator versucht, eine Verbindung mit einem Volume herzustellen, überprüft Ihre Appliance die Zugriffssteuerungseinträge, die diesem Volume zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="edaee-110">When an iSCSI initiator attempts to connect to a volume, your appliance checks the access control records assigned to that volume.</span></span>
<span data-ttu-id="edaee-111">Wenn die Parameter des iSCSI-Initiators mit einem der Einträge in einem Zugriffssteuerungseintrag übereinstimmen, der diesem Volume zugeordnet ist, kann der iSCSI-Initiator eine Verbindung herstellen.</span><span class="sxs-lookup"><span data-stu-id="edaee-111">If the iSCSI initiator parameters match one of the entries in an access control record mapped to that volume, the iSCSI initiator can connect.</span></span>

## <span data-ttu-id="edaee-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="edaee-112">EXAMPLES</span></span>

### <span data-ttu-id="edaee-113">Beispiel 1: Abrufen aller Zugriffssteuerungseinträge</span><span class="sxs-lookup"><span data-stu-id="edaee-113">Example 1: Get all access control records</span></span>
```
PS C:\>Get-AzureStorSimpleAccessControlRecord
InstanceId                           Name                        InitiatorName               VolumeCount
----------                           ----                        -------------               -----------
01a31aa5-14de-4b77-b926-2842577f540e Windows_XYUSFL718-RV_ACR    iqn.1991-05.com.microsof... 3
071c282d-0cd2-4c5f-b687-48966037ba48 Linux_XYUSFL719_ACR         iqn.1994-05.com.redhat:a... 3
4600eade-71f8-4d04-baec-0e7cf1d1e8fb Windows_XYUSFL720_ACR       iqn.1991-05.com.microsof... 9
d508d6f0-fcda-4624-b223-c0b307d6113e Linux_XYUSFL350_ACR         iqn.1991-05.com.microsof... 9
```

<span data-ttu-id="edaee-114">Dieser Befehl ruft alle Zugriffssteuerungseinträge ab.</span><span class="sxs-lookup"><span data-stu-id="edaee-114">This command gets all access control records.</span></span>

### <span data-ttu-id="edaee-115">Beispiel 2: Abrufen eines bestimmten Zugriffssteuerungseintrags</span><span class="sxs-lookup"><span data-stu-id="edaee-115">Example 2: Get a specific access control record</span></span>
```
PS C:\>Get-AzureStorSimpleAccessControlRecord -ACRName "Acr11"
VERBOSE: ClientRequestId: 61f261c7-acd3-4bcc-922a-ddfd85eb767b_PS
VERBOSE: ClientRequestId: 49c6a4c7-d299-46fd-a553-034c52b47487_PS

GlobalId            : 
InitiatorName       : iqn-contoso63
InstanceId          : 55f24643-ab3a-4098-ade2-aa2b1a3ab18c
Name                : Acr11
OperationInProgress : None
VolumeCount         : 6

VERBOSE: Access Control Record with given name Acr11 is found!
```

<span data-ttu-id="edaee-116">Dieser Befehl ruft den Zugriffssteuerungseintrag mit dem Namen Acr11 ab.</span><span class="sxs-lookup"><span data-stu-id="edaee-116">This command gets the access control record named Acr11.</span></span>

## <span data-ttu-id="edaee-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="edaee-117">PARAMETERS</span></span>

### <span data-ttu-id="edaee-118">-ACRName</span><span class="sxs-lookup"><span data-stu-id="edaee-118">-ACRName</span></span>
<span data-ttu-id="edaee-119">Gibt den Namen eines Zugriffssteuerungseintrags an, der abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="edaee-119">Specifies the name of an access control record to get.</span></span>

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

### <span data-ttu-id="edaee-120">-Profil</span><span class="sxs-lookup"><span data-stu-id="edaee-120">-Profile</span></span>
<span data-ttu-id="edaee-121">Gibt ein Azure-Profil an.</span><span class="sxs-lookup"><span data-stu-id="edaee-121">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="edaee-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="edaee-122">CommonParameters</span></span>
<span data-ttu-id="edaee-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="edaee-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="edaee-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="edaee-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="edaee-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="edaee-125">INPUTS</span></span>

### <span data-ttu-id="edaee-126">Keine</span><span class="sxs-lookup"><span data-stu-id="edaee-126">None</span></span>

## <span data-ttu-id="edaee-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="edaee-127">OUTPUTS</span></span>

### <span data-ttu-id="edaee-128">AccessControlRecord, IList\<AccessControlRecord\></span><span class="sxs-lookup"><span data-stu-id="edaee-128">AccessControlRecord, IList\<AccessControlRecord\></span></span>
<span data-ttu-id="edaee-129">Dieses Cmdlet gibt ein **AccessControlRecord** -Objekt oder **ein \<AccessControlRecord\> IList** -Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="edaee-129">This cmdlet returns an **AccessControlRecord** object or an **IList\<AccessControlRecord\>** object.</span></span>
<span data-ttu-id="edaee-130">Ein **AccessControlRecord** -Objekt enthält die folgenden Felder:</span><span class="sxs-lookup"><span data-stu-id="edaee-130">An **AccessControlRecord** object contains the following fields:</span></span> 

- <span data-ttu-id="edaee-131">**Global** -Nr ( **Zeichenfolge** )</span><span class="sxs-lookup"><span data-stu-id="edaee-131">**GlobalId** ( **String** )</span></span> 
- <span data-ttu-id="edaee-132">**Initiatorname** ( **Zeichenfolge** )</span><span class="sxs-lookup"><span data-stu-id="edaee-132">**InitiatorName** ( **String** )</span></span> 
- <span data-ttu-id="edaee-133">**InstanceId** ( **Zeichenfolge** )</span><span class="sxs-lookup"><span data-stu-id="edaee-133">**InstanceId** ( **String** )</span></span> 
- <span data-ttu-id="edaee-134">**Name** ( **Zeichenfolge** )</span><span class="sxs-lookup"><span data-stu-id="edaee-134">**Name** ( **String** )</span></span> 
- <span data-ttu-id="edaee-135">**OperationInProgress** ( **OperationInProgress** )</span><span class="sxs-lookup"><span data-stu-id="edaee-135">**OperationInProgress** ( **OperationInProgress** )</span></span> 
- <span data-ttu-id="edaee-136">**VolumeCount** ( **int** )</span><span class="sxs-lookup"><span data-stu-id="edaee-136">**VolumeCount** ( **int** )</span></span>

## <span data-ttu-id="edaee-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="edaee-137">NOTES</span></span>

## <span data-ttu-id="edaee-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="edaee-138">RELATED LINKS</span></span>

[<span data-ttu-id="edaee-139">Neu – AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="edaee-139">New-AzureStorSimpleAccessControlRecord</span></span>](./New-AzureStorSimpleAccessControlRecord.md)

[<span data-ttu-id="edaee-140">Remove-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="edaee-140">Remove-AzureStorSimpleAccessControlRecord</span></span>](./Remove-AzureStorSimpleAccessControlRecord.md)

[<span data-ttu-id="edaee-141">Satz-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="edaee-141">Set-AzureStorSimpleAccessControlRecord</span></span>](./Set-AzureStorSimpleAccessControlRecord.md)


