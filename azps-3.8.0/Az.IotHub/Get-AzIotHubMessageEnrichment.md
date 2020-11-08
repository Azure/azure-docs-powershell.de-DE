---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubmessageenrichment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubMessageEnrichment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubMessageEnrichment.md
ms.openlocfilehash: 91694efaeaf1a24018269706f3ee388feb7218ea
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93995527"
---
# <span data-ttu-id="9d566-101">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="9d566-101">Get-AzIotHubMessageEnrichment</span></span>

## <span data-ttu-id="9d566-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9d566-102">SYNOPSIS</span></span>
<span data-ttu-id="9d566-103">Listet alle Nachrichten-Anreicherungen oder eine bestimmte Nachrichten Anreicherung für Ihre viel-Nabe auf.</span><span class="sxs-lookup"><span data-stu-id="9d566-103">Lists all message enrichments or a particular message enrichment for your IoT Hub.</span></span>

## <span data-ttu-id="9d566-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9d566-104">SYNTAX</span></span>

### <span data-ttu-id="9d566-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="9d566-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubMessageEnrichment [-ResourceGroupName] <String> [-Name] <String> [-Key <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9d566-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="9d566-106">InputObjectSet</span></span>
```
Get-AzIotHubMessageEnrichment [-InputObject] <PSIotHub> [-Key <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9d566-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="9d566-107">ResourceIdSet</span></span>
```
Get-AzIotHubMessageEnrichment [-ResourceId] <String> [-Key <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9d566-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9d566-108">DESCRIPTION</span></span>
<span data-ttu-id="9d566-109">Eine ausführliche Erläuterung der Nachrichten Anreicherung in Azure viel Hub finden Sie unter https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span><span class="sxs-lookup"><span data-stu-id="9d566-109">For a detailed explanation of message enrichments in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span></span>

## <span data-ttu-id="9d566-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9d566-110">EXAMPLES</span></span>

### <span data-ttu-id="9d566-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="9d566-111">Example 1</span></span>
```powershell
PS C:\>  Get-AzIotHubMessageEnrichment -ResourceGroupName "myresourcegroup" -Name "myiothub"

Key  Value   Endpoint(s)
---  -----   -----------
key1 value1  {endpoint1, endpoint2}
key2 value2  {endpoint3, endpoint4}
```

<span data-ttu-id="9d566-112">Auflisten aller Nachrichten Anreicherungen in MyIotHub</span><span class="sxs-lookup"><span data-stu-id="9d566-112">List all message enrichments in MyIotHub</span></span>

### <span data-ttu-id="9d566-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="9d566-113">Example 2</span></span>
```powershell
PS C:\>  Get-AzIotHubMessageEnrichment -ResourceGroupName "myresourcegroup" -Name "myiothub" -Key "newKey"

Key         : key1
Value       : value1
Endpoint(s) : {endpoint1, endpoint2}
```

<span data-ttu-id="9d566-114">Details zur "newkey"-Nachrichten Anreicherung anzeigen.</span><span class="sxs-lookup"><span data-stu-id="9d566-114">Show details about "newKey" message enrichment.</span></span>

## <span data-ttu-id="9d566-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="9d566-115">PARAMETERS</span></span>

### <span data-ttu-id="9d566-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d566-116">-DefaultProfile</span></span>
<span data-ttu-id="9d566-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9d566-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d566-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="9d566-118">-InputObject</span></span>
<span data-ttu-id="9d566-119">IotHub-Objekt</span><span class="sxs-lookup"><span data-stu-id="9d566-119">IotHub object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9d566-120">-Taste</span><span class="sxs-lookup"><span data-stu-id="9d566-120">-Key</span></span>
<span data-ttu-id="9d566-121">Der Schlüssel der Bereicherung.</span><span class="sxs-lookup"><span data-stu-id="9d566-121">The enrichment's key.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d566-122">-Name</span><span class="sxs-lookup"><span data-stu-id="9d566-122">-Name</span></span>
<span data-ttu-id="9d566-123">Name des viel-Hubs</span><span class="sxs-lookup"><span data-stu-id="9d566-123">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d566-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9d566-124">-ResourceGroupName</span></span>
<span data-ttu-id="9d566-125">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="9d566-125">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d566-126">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="9d566-126">-ResourceId</span></span>
<span data-ttu-id="9d566-127">IotHub-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="9d566-127">IotHub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d566-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d566-128">CommonParameters</span></span>
<span data-ttu-id="9d566-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d566-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d566-130">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d566-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d566-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9d566-131">INPUTS</span></span>

### <span data-ttu-id="9d566-132">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="9d566-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="9d566-133">System. String</span><span class="sxs-lookup"><span data-stu-id="9d566-133">System.String</span></span>

## <span data-ttu-id="9d566-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9d566-134">OUTPUTS</span></span>

### <span data-ttu-id="9d566-135">Microsoft. Azure. Commands. Management. IotHub. Models. PSEnrichmentMetadata</span><span class="sxs-lookup"><span data-stu-id="9d566-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSEnrichmentMetadata</span></span>

### <span data-ttu-id="9d566-136">Microsoft. Azure. Commands. Management. IotHub. Models. PSEnrichmentProperties []</span><span class="sxs-lookup"><span data-stu-id="9d566-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSEnrichmentProperties[]</span></span>

## <span data-ttu-id="9d566-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="9d566-137">NOTES</span></span>

## <span data-ttu-id="9d566-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9d566-138">RELATED LINKS</span></span>
