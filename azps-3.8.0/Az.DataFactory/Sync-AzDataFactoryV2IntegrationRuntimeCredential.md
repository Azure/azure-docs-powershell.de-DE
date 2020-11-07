---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/sync-azdatafactoryv2integrationruntimecredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Sync-AzDataFactoryV2IntegrationRuntimeCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Sync-AzDataFactoryV2IntegrationRuntimeCredential.md
ms.openlocfilehash: cb9362a64b58770beb7d3b70f989fc740a2fc00e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93847080"
---
# <span data-ttu-id="cff5c-101">Sync-AzDataFactoryV2IntegrationRuntimeCredential</span><span class="sxs-lookup"><span data-stu-id="cff5c-101">Sync-AzDataFactoryV2IntegrationRuntimeCredential</span></span>

## <span data-ttu-id="cff5c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="cff5c-102">SYNOPSIS</span></span>
<span data-ttu-id="cff5c-103">Synchronisiert Anmeldeinformationen zwischen Integrationslauf Zeit Knoten.</span><span class="sxs-lookup"><span data-stu-id="cff5c-103">Synchronizes credentials among integration runtime nodes.</span></span>

## <span data-ttu-id="cff5c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="cff5c-104">SYNTAX</span></span>

### <span data-ttu-id="cff5c-105">ByIntegrationRuntimeName (Standard)</span><span class="sxs-lookup"><span data-stu-id="cff5c-105">ByIntegrationRuntimeName (Default)</span></span>
```
Sync-AzDataFactoryV2IntegrationRuntimeCredential [-Force] [-IntegrationRuntimeName] <String>
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cff5c-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="cff5c-106">ByResourceId</span></span>
```
Sync-AzDataFactoryV2IntegrationRuntimeCredential [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cff5c-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="cff5c-107">ByIntegrationRuntimeObject</span></span>
```
Sync-AzDataFactoryV2IntegrationRuntimeCredential [-Force] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cff5c-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cff5c-108">DESCRIPTION</span></span>
<span data-ttu-id="cff5c-109">Das Cmdlet " **Sync-AzDataFactoryV2IntegrationRuntimeCredential** " synchronisiert lokale Anmeldeinformationen zwischen Integrationslauf Zeit Knoten, wodurch die Anmeldeinformationen in allen Knoten identisch sind.</span><span class="sxs-lookup"><span data-stu-id="cff5c-109">The **Sync-AzDataFactoryV2IntegrationRuntimeCredential** cmdlet synchronizes on-premises credentials among integration runtime nodes, which forces the credentials to be identical in all nodes.</span></span>

## <span data-ttu-id="cff5c-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="cff5c-110">EXAMPLES</span></span>

### <span data-ttu-id="cff5c-111">Beispiel 1: Synchronisieren einer Integration Runtime-Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="cff5c-111">Example 1: Sync an integration runtime credential</span></span>
```
PS C:\> Sync-AzDataFactoryV2IntegrationRuntimeCredential -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir'
```

<span data-ttu-id="cff5c-112">Mit dem Cmdlet werden die Anmeldeinformationen zwischen Integrationslauf Zeit Knoten synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="cff5c-112">The cmdlet synchronizes credentials among integration runtime nodes.</span></span>

## <span data-ttu-id="cff5c-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="cff5c-113">PARAMETERS</span></span>

### <span data-ttu-id="cff5c-114">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="cff5c-114">-DataFactoryName</span></span>
<span data-ttu-id="cff5c-115">Der Name der Daten Factory.</span><span class="sxs-lookup"><span data-stu-id="cff5c-115">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cff5c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cff5c-116">-DefaultProfile</span></span>
<span data-ttu-id="cff5c-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="cff5c-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cff5c-118">-Force</span><span class="sxs-lookup"><span data-stu-id="cff5c-118">-Force</span></span>
<span data-ttu-id="cff5c-119">Führt das Cmdlet ohne Aufforderung zur Bestätigung aus.</span><span class="sxs-lookup"><span data-stu-id="cff5c-119">Runs the cmdlet without prompting for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cff5c-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="cff5c-120">-InputObject</span></span>
<span data-ttu-id="cff5c-121">Das Integrationslauf Zeit Objekt.</span><span class="sxs-lookup"><span data-stu-id="cff5c-121">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime
Parameter Sets: ByIntegrationRuntimeObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cff5c-122">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="cff5c-122">-IntegrationRuntimeName</span></span>
<span data-ttu-id="cff5c-123">Der Name der Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="cff5c-123">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cff5c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cff5c-124">-ResourceGroupName</span></span>
<span data-ttu-id="cff5c-125">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="cff5c-125">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cff5c-126">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="cff5c-126">-ResourceId</span></span>
<span data-ttu-id="cff5c-127">Die Azure-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="cff5c-127">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cff5c-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="cff5c-128">-Confirm</span></span>
<span data-ttu-id="cff5c-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="cff5c-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cff5c-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cff5c-130">-WhatIf</span></span>
<span data-ttu-id="cff5c-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird, das Cmdlet aber nicht ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="cff5c-131">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cff5c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cff5c-132">CommonParameters</span></span>
<span data-ttu-id="cff5c-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cff5c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cff5c-134">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cff5c-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cff5c-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="cff5c-135">INPUTS</span></span>

### <span data-ttu-id="cff5c-136">System. String</span><span class="sxs-lookup"><span data-stu-id="cff5c-136">System.String</span></span>

### <span data-ttu-id="cff5c-137">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="cff5c-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="cff5c-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="cff5c-138">OUTPUTS</span></span>

### <span data-ttu-id="cff5c-139">System. void</span><span class="sxs-lookup"><span data-stu-id="cff5c-139">System.Void</span></span>

## <span data-ttu-id="cff5c-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="cff5c-140">NOTES</span></span>

## <span data-ttu-id="cff5c-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="cff5c-141">RELATED LINKS</span></span>
