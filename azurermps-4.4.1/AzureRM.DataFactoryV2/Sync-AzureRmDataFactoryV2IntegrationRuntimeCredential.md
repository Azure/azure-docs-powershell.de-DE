---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: 63889ce74af1051211a579d1af7cc54be14822f5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662431"
---
# <span data-ttu-id="a90eb-101">Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential</span><span class="sxs-lookup"><span data-stu-id="a90eb-101">Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential</span></span>

## <span data-ttu-id="a90eb-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a90eb-102">SYNOPSIS</span></span>
<span data-ttu-id="a90eb-103">Synchronisiert Anmeldeinformationen zwischen Integrationslauf Zeit Knoten.</span><span class="sxs-lookup"><span data-stu-id="a90eb-103">Synchronizes credentials among integration runtime nodes.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a90eb-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a90eb-104">SYNTAX</span></span>

### <span data-ttu-id="a90eb-105">ByIntegrationRuntimeName (Standard)</span><span class="sxs-lookup"><span data-stu-id="a90eb-105">ByIntegrationRuntimeName (Default)</span></span>
```
Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential [-Force] [-IntegrationRuntimeName] <String>
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-WhatIf] [-Confirm]
```

### <span data-ttu-id="a90eb-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="a90eb-106">ByResourceId</span></span>
```
Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential [-Force] [-ResourceId] <String> [-WhatIf] [-Confirm]
```

### <span data-ttu-id="a90eb-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="a90eb-107">ByIntegrationRuntimeObject</span></span>
```
Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential [-Force] [-InputObject] <PSIntegrationRuntime>
 [-WhatIf] [-Confirm]
```

## <span data-ttu-id="a90eb-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a90eb-108">DESCRIPTION</span></span>
<span data-ttu-id="a90eb-109">Das Cmdlet " **Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential** " synchronisiert lokale Anmeldeinformationen zwischen Integrationslauf Zeit Knoten, wodurch die Anmeldeinformationen in allen Knoten identisch sind.</span><span class="sxs-lookup"><span data-stu-id="a90eb-109">The **Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential** cmdlet synchronizes on-premises credentials among integration runtime nodes, which forces the credentials to be identical in all nodes.</span></span>

## <span data-ttu-id="a90eb-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a90eb-110">EXAMPLES</span></span>

### <span data-ttu-id="a90eb-111">Beispiel 1: Synchronisieren einer Integration Runtime-Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="a90eb-111">Example 1: Sync an integration runtime credential</span></span>
```
PS C:\> Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir'
```

<span data-ttu-id="a90eb-112">Mit dem Cmdlet werden die Anmeldeinformationen zwischen Integrationslauf Zeit Knoten synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="a90eb-112">The cmdlet synchronizes credentials among integration runtime nodes.</span></span>

## <span data-ttu-id="a90eb-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="a90eb-113">PARAMETERS</span></span>

### <span data-ttu-id="a90eb-114">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a90eb-114">-Confirm</span></span>
<span data-ttu-id="a90eb-115">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a90eb-115">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a90eb-116">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="a90eb-116">-DataFactoryName</span></span>
<span data-ttu-id="a90eb-117">Der Name der Daten Factory.</span><span class="sxs-lookup"><span data-stu-id="a90eb-117">The data factory name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a90eb-118">-Force</span><span class="sxs-lookup"><span data-stu-id="a90eb-118">-Force</span></span>
<span data-ttu-id="a90eb-119">Führt das Cmdlet ohne Aufforderung zur Bestätigung aus.</span><span class="sxs-lookup"><span data-stu-id="a90eb-119">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="a90eb-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="a90eb-120">-InputObject</span></span>
<span data-ttu-id="a90eb-121">Das Integrationslauf Zeit Objekt.</span><span class="sxs-lookup"><span data-stu-id="a90eb-121">The integration runtime object.</span></span>

```yaml
Type: PSIntegrationRuntime
Parameter Sets: ByIntegrationRuntimeObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a90eb-122">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="a90eb-122">-IntegrationRuntimeName</span></span>
<span data-ttu-id="a90eb-123">Der Name der Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="a90eb-123">The integration runtime name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a90eb-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a90eb-124">-ResourceGroupName</span></span>
<span data-ttu-id="a90eb-125">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="a90eb-125">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a90eb-126">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="a90eb-126">-ResourceId</span></span>
<span data-ttu-id="a90eb-127">Die Azure-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="a90eb-127">The Azure resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a90eb-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a90eb-128">-WhatIf</span></span>
<span data-ttu-id="a90eb-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird, das Cmdlet aber nicht ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a90eb-129">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="a90eb-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a90eb-130">INPUTS</span></span>

### <span data-ttu-id="a90eb-131">System. String</span><span class="sxs-lookup"><span data-stu-id="a90eb-131">System.String</span></span>
<span data-ttu-id="a90eb-132">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="a90eb-132">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>


## <span data-ttu-id="a90eb-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a90eb-133">OUTPUTS</span></span>

### <span data-ttu-id="a90eb-134">System. Object</span><span class="sxs-lookup"><span data-stu-id="a90eb-134">System.Object</span></span>

## <span data-ttu-id="a90eb-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="a90eb-135">NOTES</span></span>

## <span data-ttu-id="a90eb-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a90eb-136">RELATED LINKS</span></span>
