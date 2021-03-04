---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/get-aziothubmessageenrichment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubMessageEnrichment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubMessageEnrichment.md
ms.openlocfilehash: 18a6d5db9ecf7cf02604a883b49545650413ee28
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101936856"
---
# <span data-ttu-id="98f79-101">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="98f79-101">Get-AzIotHubMessageEnrichment</span></span>

## <span data-ttu-id="98f79-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="98f79-102">SYNOPSIS</span></span>
<span data-ttu-id="98f79-103">Listet alle Nachrichtenanreicherungen oder eine bestimmte Nachrichtenanreicherung für Ihren IoT Hub auf.</span><span class="sxs-lookup"><span data-stu-id="98f79-103">Lists all message enrichments or a particular message enrichment for your IoT Hub.</span></span>

## <span data-ttu-id="98f79-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="98f79-104">SYNTAX</span></span>

### <span data-ttu-id="98f79-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="98f79-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubMessageEnrichment [-ResourceGroupName] <String> [-Name] <String> [-Key <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="98f79-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="98f79-106">InputObjectSet</span></span>
```
Get-AzIotHubMessageEnrichment [-InputObject] <PSIotHub> [-Key <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="98f79-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="98f79-107">ResourceIdSet</span></span>
```
Get-AzIotHubMessageEnrichment [-ResourceId] <String> [-Key <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="98f79-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="98f79-108">DESCRIPTION</span></span>
<span data-ttu-id="98f79-109">Eine detaillierte Erläuterung der Nachrichtenanreicherungen in Azure IoT Hub finden Sie unter https://docs.microsoft.com/azure/iot-hub/iot-hub-message-enrichments-overview</span><span class="sxs-lookup"><span data-stu-id="98f79-109">For a detailed explanation of message enrichments in Azure IoT Hub, see https://docs.microsoft.com/azure/iot-hub/iot-hub-message-enrichments-overview</span></span>

## <span data-ttu-id="98f79-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="98f79-110">EXAMPLES</span></span>

### <span data-ttu-id="98f79-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="98f79-111">Example 1</span></span>
```powershell
PS C:\>  Get-AzIotHubMessageEnrichment -ResourceGroupName "myresourcegroup" -Name "myiothub"

Key  Value   Endpoint(s)
---  -----   -----------
key1 value1  {endpoint1, endpoint2}
key2 value2  {endpoint3, endpoint4}
```

<span data-ttu-id="98f79-112">Auflisten aller Nachrichtenanreicherungen in MyIotHub</span><span class="sxs-lookup"><span data-stu-id="98f79-112">List all message enrichments in MyIotHub</span></span>

### <span data-ttu-id="98f79-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="98f79-113">Example 2</span></span>
```powershell
PS C:\>  Get-AzIotHubMessageEnrichment -ResourceGroupName "myresourcegroup" -Name "myiothub" -Key "newKey"

Key         : key1
Value       : value1
Endpoint(s) : {endpoint1, endpoint2}
```

<span data-ttu-id="98f79-114">Details zur Nachrichtenanreicherung "newKey" anzeigen</span><span class="sxs-lookup"><span data-stu-id="98f79-114">Show details about "newKey" message enrichment.</span></span>

## <span data-ttu-id="98f79-115">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="98f79-115">PARAMETERS</span></span>

### <span data-ttu-id="98f79-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98f79-116">-DefaultProfile</span></span>
<span data-ttu-id="98f79-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="98f79-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="98f79-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="98f79-118">-InputObject</span></span>
<span data-ttu-id="98f79-119">IotHub-Objekt</span><span class="sxs-lookup"><span data-stu-id="98f79-119">IotHub object</span></span>

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

### <span data-ttu-id="98f79-120">-Key</span><span class="sxs-lookup"><span data-stu-id="98f79-120">-Key</span></span>
<span data-ttu-id="98f79-121">Der Schlüssel der Bereicherung.</span><span class="sxs-lookup"><span data-stu-id="98f79-121">The enrichment's key.</span></span>

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

### <span data-ttu-id="98f79-122">-Name</span><span class="sxs-lookup"><span data-stu-id="98f79-122">-Name</span></span>
<span data-ttu-id="98f79-123">Name des Iot-Hubs</span><span class="sxs-lookup"><span data-stu-id="98f79-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="98f79-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98f79-124">-ResourceGroupName</span></span>
<span data-ttu-id="98f79-125">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="98f79-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="98f79-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="98f79-126">-ResourceId</span></span>
<span data-ttu-id="98f79-127">IotHub-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="98f79-127">IotHub Resource Id</span></span>

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

### <span data-ttu-id="98f79-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98f79-128">CommonParameters</span></span>
<span data-ttu-id="98f79-129">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98f79-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98f79-130">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98f79-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98f79-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="98f79-131">INPUTS</span></span>

### <span data-ttu-id="98f79-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="98f79-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="98f79-133">System.String</span><span class="sxs-lookup"><span data-stu-id="98f79-133">System.String</span></span>

## <span data-ttu-id="98f79-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="98f79-134">OUTPUTS</span></span>

### <span data-ttu-id="98f79-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSEnrichmentMetadata</span><span class="sxs-lookup"><span data-stu-id="98f79-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSEnrichmentMetadata</span></span>

### <span data-ttu-id="98f79-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSEnrichmentProperties[]</span><span class="sxs-lookup"><span data-stu-id="98f79-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSEnrichmentProperties[]</span></span>

## <span data-ttu-id="98f79-137">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="98f79-137">NOTES</span></span>

## <span data-ttu-id="98f79-138">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="98f79-138">RELATED LINKS</span></span>
