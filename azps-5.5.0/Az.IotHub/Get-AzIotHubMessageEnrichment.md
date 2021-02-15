---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubmessageenrichment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubMessageEnrichment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubMessageEnrichment.md
ms.openlocfilehash: 91694efaeaf1a24018269706f3ee388feb7218ea
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100152921"
---
# <span data-ttu-id="4292b-101">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="4292b-101">Get-AzIotHubMessageEnrichment</span></span>

## <span data-ttu-id="4292b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4292b-102">SYNOPSIS</span></span>
<span data-ttu-id="4292b-103">Listet alle Nachrichtenanreicherungen oder eine bestimmte Nachrichtenanreicherung für Ihren IoT Hub auf.</span><span class="sxs-lookup"><span data-stu-id="4292b-103">Lists all message enrichments or a particular message enrichment for your IoT Hub.</span></span>

## <span data-ttu-id="4292b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4292b-104">SYNTAX</span></span>

### <span data-ttu-id="4292b-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="4292b-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubMessageEnrichment [-ResourceGroupName] <String> [-Name] <String> [-Key <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4292b-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="4292b-106">InputObjectSet</span></span>
```
Get-AzIotHubMessageEnrichment [-InputObject] <PSIotHub> [-Key <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4292b-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="4292b-107">ResourceIdSet</span></span>
```
Get-AzIotHubMessageEnrichment [-ResourceId] <String> [-Key <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4292b-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4292b-108">DESCRIPTION</span></span>
<span data-ttu-id="4292b-109">Eine ausführliche Erläuterung der Nachrichtenanreicherung in Azure IoT Hub finden Sie unter https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span><span class="sxs-lookup"><span data-stu-id="4292b-109">For a detailed explanation of message enrichments in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span></span>

## <span data-ttu-id="4292b-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4292b-110">EXAMPLES</span></span>

### <span data-ttu-id="4292b-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4292b-111">Example 1</span></span>
```powershell
PS C:\>  Get-AzIotHubMessageEnrichment -ResourceGroupName "myresourcegroup" -Name "myiothub"

Key  Value   Endpoint(s)
---  -----   -----------
key1 value1  {endpoint1, endpoint2}
key2 value2  {endpoint3, endpoint4}
```

<span data-ttu-id="4292b-112">Auflisten aller Nachrichtenanreicherungen in MyIotHub</span><span class="sxs-lookup"><span data-stu-id="4292b-112">List all message enrichments in MyIotHub</span></span>

### <span data-ttu-id="4292b-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="4292b-113">Example 2</span></span>
```powershell
PS C:\>  Get-AzIotHubMessageEnrichment -ResourceGroupName "myresourcegroup" -Name "myiothub" -Key "newKey"

Key         : key1
Value       : value1
Endpoint(s) : {endpoint1, endpoint2}
```

<span data-ttu-id="4292b-114">Zeigen Sie Details zur Nachrichtenanreicherung "newKey" an.</span><span class="sxs-lookup"><span data-stu-id="4292b-114">Show details about "newKey" message enrichment.</span></span>

## <span data-ttu-id="4292b-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4292b-115">PARAMETERS</span></span>

### <span data-ttu-id="4292b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4292b-116">-DefaultProfile</span></span>
<span data-ttu-id="4292b-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4292b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4292b-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4292b-118">-InputObject</span></span>
<span data-ttu-id="4292b-119">IotHub-Objekt</span><span class="sxs-lookup"><span data-stu-id="4292b-119">IotHub object</span></span>

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

### <span data-ttu-id="4292b-120">-Key</span><span class="sxs-lookup"><span data-stu-id="4292b-120">-Key</span></span>
<span data-ttu-id="4292b-121">Schlüssel der Anreicherung</span><span class="sxs-lookup"><span data-stu-id="4292b-121">The enrichment's key.</span></span>

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

### <span data-ttu-id="4292b-122">-Name</span><span class="sxs-lookup"><span data-stu-id="4292b-122">-Name</span></span>
<span data-ttu-id="4292b-123">Name des Iot Hub</span><span class="sxs-lookup"><span data-stu-id="4292b-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="4292b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4292b-124">-ResourceGroupName</span></span>
<span data-ttu-id="4292b-125">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="4292b-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="4292b-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4292b-126">-ResourceId</span></span>
<span data-ttu-id="4292b-127">IotHub-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="4292b-127">IotHub Resource Id</span></span>

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

### <span data-ttu-id="4292b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4292b-128">CommonParameters</span></span>
<span data-ttu-id="4292b-129">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4292b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4292b-130">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4292b-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4292b-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4292b-131">INPUTS</span></span>

### <span data-ttu-id="4292b-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="4292b-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="4292b-133">System.String</span><span class="sxs-lookup"><span data-stu-id="4292b-133">System.String</span></span>

## <span data-ttu-id="4292b-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4292b-134">OUTPUTS</span></span>

### <span data-ttu-id="4292b-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSEnrichmentMetadata</span><span class="sxs-lookup"><span data-stu-id="4292b-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSEnrichmentMetadata</span></span>

### <span data-ttu-id="4292b-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSEnrichmentProperties[]</span><span class="sxs-lookup"><span data-stu-id="4292b-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSEnrichmentProperties[]</span></span>

## <span data-ttu-id="4292b-137">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="4292b-137">NOTES</span></span>

## <span data-ttu-id="4292b-138">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="4292b-138">RELATED LINKS</span></span>
