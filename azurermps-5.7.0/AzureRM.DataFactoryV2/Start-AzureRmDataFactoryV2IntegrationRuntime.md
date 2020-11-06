---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/start-azurermdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Start-AzureRmDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Start-AzureRmDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: 77c06c871d35223f296a7f318460b868e8ad0320
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93478510"
---
# <span data-ttu-id="e2c18-101">Start-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="e2c18-101">Start-AzureRmDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="e2c18-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e2c18-102">SYNOPSIS</span></span>
<span data-ttu-id="e2c18-103">Startet eine verwaltete dedizierte Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="e2c18-103">Starts a managed dedicated integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e2c18-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e2c18-104">SYNTAX</span></span>

### <span data-ttu-id="e2c18-105">ByIntegrationRuntimeName (Standard)</span><span class="sxs-lookup"><span data-stu-id="e2c18-105">ByIntegrationRuntimeName (Default)</span></span>
```
Start-AzureRmDataFactoryV2IntegrationRuntime [-Force] [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e2c18-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="e2c18-106">ByResourceId</span></span>
```
Start-AzureRmDataFactoryV2IntegrationRuntime [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e2c18-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="e2c18-107">ByIntegrationRuntimeObject</span></span>
```
Start-AzureRmDataFactoryV2IntegrationRuntime [-Force] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e2c18-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e2c18-108">DESCRIPTION</span></span>
<span data-ttu-id="e2c18-109">Das Cmdlet **Start-AzureRmDataFactoryV2IntegrationRuntime** startet eine verwaltete dedizierte Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="e2c18-109">The **Start-AzureRmDataFactoryV2IntegrationRuntime** cmdlet starts a managed dedicated integration runtime.</span></span> <span data-ttu-id="e2c18-110">Die Ressource wird bereitgestellt, und nach dem Vorgang wird der Zustand "gestartet".</span><span class="sxs-lookup"><span data-stu-id="e2c18-110">The resource is provisioned and after the operation the state is 'Started'.</span></span>

## <span data-ttu-id="e2c18-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e2c18-111">EXAMPLES</span></span>

### <span data-ttu-id="e2c18-112">Beispiel 1: Starten einer Integrationslaufzeit</span><span class="sxs-lookup"><span data-stu-id="e2c18-112">Example 1: Start an integration runtime</span></span>
```
PS C:\> Start-AzureRmDataFactoryV2IntegrationRuntime -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name test-dedicated-ir' -Force

    CreateTime                   : 9/11/2017 2:16:12 PM
    Nodes                        : {tvm-1650185656_1-20170911t141751z}
    OtherErrors                  : {}
    LastOperation                : 
    State                        : Started
    Location                     : West US
    NodeSize                     : Standard_D1_v2
    NodeCount                    : 1
    MaxParallelExecutionsPerNode : 1
    CatalogServerEndpoint        : testsvr.database.windows.net
    CatalogAdminUserName         : admin
    CatalogAdminPassword         : **********
    CatalogPricingTier           : S1
    VNetId                       : 
    Subnet                       : 
    Id                           : /subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-dedicated-ir
    ResourceGroupName            : rg-test-dfv2
    DataFactoryName              : test-df-eu2
    Name                         : test-dedicated-ir
    Description                  : Reserved IR
```

<span data-ttu-id="e2c18-113">Mit diesem Cmdlet wird eine verwaltete dedizierte Integrationslaufzeit mit dem Namen "Test-dediziert-IR" gestartet.</span><span class="sxs-lookup"><span data-stu-id="e2c18-113">This cmdlet starts a managed dedicated integration runtime named 'test-dedicated-ir'.</span></span>

## <span data-ttu-id="e2c18-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="e2c18-114">PARAMETERS</span></span>

### <span data-ttu-id="e2c18-115">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="e2c18-115">-DataFactoryName</span></span>
<span data-ttu-id="e2c18-116">Der Name der Daten Factory.</span><span class="sxs-lookup"><span data-stu-id="e2c18-116">The data factory name.</span></span>

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

### <span data-ttu-id="e2c18-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2c18-117">-DefaultProfile</span></span>
<span data-ttu-id="e2c18-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e2c18-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2c18-119">-Force</span><span class="sxs-lookup"><span data-stu-id="e2c18-119">-Force</span></span>
<span data-ttu-id="e2c18-120">Führt das Cmdlet ohne Aufforderung zur Bestätigung aus.</span><span class="sxs-lookup"><span data-stu-id="e2c18-120">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="e2c18-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="e2c18-121">-InputObject</span></span>
<span data-ttu-id="e2c18-122">Das Integrationslauf Zeit Objekt.</span><span class="sxs-lookup"><span data-stu-id="e2c18-122">The integration runtime object.</span></span>

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

### <span data-ttu-id="e2c18-123">-Name</span><span class="sxs-lookup"><span data-stu-id="e2c18-123">-Name</span></span>
<span data-ttu-id="e2c18-124">Der Name der Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="e2c18-124">The integration runtime name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: IntegrationRuntimeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2c18-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2c18-125">-ResourceGroupName</span></span>
<span data-ttu-id="e2c18-126">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="e2c18-126">The resource group name.</span></span>

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

### <span data-ttu-id="e2c18-127">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="e2c18-127">-ResourceId</span></span>
<span data-ttu-id="e2c18-128">Die Azure-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="e2c18-128">The Azure resource ID.</span></span>

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

### <span data-ttu-id="e2c18-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e2c18-129">-Confirm</span></span>
<span data-ttu-id="e2c18-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e2c18-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e2c18-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2c18-131">-WhatIf</span></span>
<span data-ttu-id="e2c18-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird, das Cmdlet aber nicht ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e2c18-132">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="e2c18-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2c18-133">CommonParameters</span></span>
<span data-ttu-id="e2c18-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2c18-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2c18-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2c18-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2c18-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e2c18-136">INPUTS</span></span>

### <span data-ttu-id="e2c18-137">System. String</span><span class="sxs-lookup"><span data-stu-id="e2c18-137">System.String</span></span>
<span data-ttu-id="e2c18-138">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="e2c18-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="e2c18-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e2c18-139">OUTPUTS</span></span>

### <span data-ttu-id="e2c18-140">Microsoft. Azure. Commands. DataFactoryV2. Models. PSManagedIntegrationRuntimeStatus</span><span class="sxs-lookup"><span data-stu-id="e2c18-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSManagedIntegrationRuntimeStatus</span></span>

## <span data-ttu-id="e2c18-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="e2c18-141">NOTES</span></span>

## <span data-ttu-id="e2c18-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e2c18-142">RELATED LINKS</span></span>

[<span data-ttu-id="e2c18-143">Stopp-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="e2c18-143">Stop-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()
