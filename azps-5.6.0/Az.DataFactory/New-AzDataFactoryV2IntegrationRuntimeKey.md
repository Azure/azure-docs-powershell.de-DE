---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/new-azdatafactoryv2integrationruntimekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryV2IntegrationRuntimeKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryV2IntegrationRuntimeKey.md
ms.openlocfilehash: 11d87742e34ae387f765551f93add5a1c300421a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101928208"
---
# <span data-ttu-id="443f6-101">New-AzDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="443f6-101">New-AzDataFactoryV2IntegrationRuntimeKey</span></span>

## <span data-ttu-id="443f6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="443f6-102">SYNOPSIS</span></span>
<span data-ttu-id="443f6-103">Regenerieren Sie den selbst gehosteten Integrations-Runtime-Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="443f6-103">Regenerate self-hosted integration runtime key.</span></span>

## <span data-ttu-id="443f6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="443f6-104">SYNTAX</span></span>

### <span data-ttu-id="443f6-105">ByIntegrationRuntimeName (Standard)</span><span class="sxs-lookup"><span data-stu-id="443f6-105">ByIntegrationRuntimeName (Default)</span></span>
```
New-AzDataFactoryV2IntegrationRuntimeKey -KeyName <String> [-Force] [-Name] <String>
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="443f6-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="443f6-106">ByResourceId</span></span>
```
New-AzDataFactoryV2IntegrationRuntimeKey -KeyName <String> [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="443f6-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="443f6-107">ByIntegrationRuntimeObject</span></span>
```
New-AzDataFactoryV2IntegrationRuntimeKey -KeyName <String> [-Force] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="443f6-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="443f6-108">DESCRIPTION</span></span>
<span data-ttu-id="443f6-109">Das Cmdlet **New-AzDataFactoryV2IntegrationRuntimeKey** regeneriert den Integrations-Runtime-Schlüssel mit dem Schlüsselnamen, der durch den Parameter "KeyName" angegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="443f6-109">The cmdlet **New-AzDataFactoryV2IntegrationRuntimeKey** regenerates the integration runtime key with the key name specified by 'KeyName' parameter.</span></span> <span data-ttu-id="443f6-110">Der vorherige Schlüssel ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="443f6-110">The previous key will is invalid.</span></span>

## <span data-ttu-id="443f6-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="443f6-111">EXAMPLES</span></span>

### <span data-ttu-id="443f6-112">Beispiel 1: Generieren eines neuen Schlüssels für eine Integrationslaufzeit</span><span class="sxs-lookup"><span data-stu-id="443f6-112">Example 1: Generate a new key for an integration runtime</span></span>
```
PS C:\> New-AzDataFactoryV2IntegrationRuntimeKey -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' -KeyName authKey2

AuthKey1 AuthKey2
-------- --------
         IR@89895504-f647-48fd-8dd3-42fa556d67e3@***
```

<span data-ttu-id="443f6-113">Das Cmdlet generiert den Schlüssel "authKey2" für die Integrationslaufzeit mit dem Namen "test-selfhost-ir".</span><span class="sxs-lookup"><span data-stu-id="443f6-113">The cmdlet regenerates key 'authKey2' for integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="443f6-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="443f6-114">PARAMETERS</span></span>

### <span data-ttu-id="443f6-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="443f6-115">-DataFactoryName</span></span>
<span data-ttu-id="443f6-116">Der Name der Datenfabrik.</span><span class="sxs-lookup"><span data-stu-id="443f6-116">The data factory name.</span></span>

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

### <span data-ttu-id="443f6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="443f6-117">-DefaultProfile</span></span>
<span data-ttu-id="443f6-118">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="443f6-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="443f6-119">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="443f6-119">-Force</span></span>
<span data-ttu-id="443f6-120">Führt das Cmdlet aus, ohne zur Bestätigung aufgefordert zu werden.</span><span class="sxs-lookup"><span data-stu-id="443f6-120">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="443f6-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="443f6-121">-InputObject</span></span>
<span data-ttu-id="443f6-122">Das Integrations-Runtime-Objekt.</span><span class="sxs-lookup"><span data-stu-id="443f6-122">The integration runtime object.</span></span>

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

### <span data-ttu-id="443f6-123">-KeyName</span><span class="sxs-lookup"><span data-stu-id="443f6-123">-KeyName</span></span>
<span data-ttu-id="443f6-124">Der Authentifizierungsschlüsselname der selbst gehosteten Integrations-Runtime.</span><span class="sxs-lookup"><span data-stu-id="443f6-124">The authentication key name of the self-hosted integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: AuthKey1, AuthKey2

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="443f6-125">-Name</span><span class="sxs-lookup"><span data-stu-id="443f6-125">-Name</span></span>
<span data-ttu-id="443f6-126">Der Name der Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="443f6-126">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases: IntegrationRuntimeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="443f6-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="443f6-127">-ResourceGroupName</span></span>
<span data-ttu-id="443f6-128">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="443f6-128">The resource group name.</span></span>

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

### <span data-ttu-id="443f6-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="443f6-129">-ResourceId</span></span>
<span data-ttu-id="443f6-130">Die Azure-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="443f6-130">The Azure resource ID.</span></span>

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

### <span data-ttu-id="443f6-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="443f6-131">-Confirm</span></span>
<span data-ttu-id="443f6-132">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="443f6-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="443f6-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="443f6-133">-WhatIf</span></span>
<span data-ttu-id="443f6-134">Zeigt, was geschieht, wenn das Cmdlet ausgeführt wird, das Cmdlet aber nicht ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="443f6-134">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="443f6-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="443f6-135">CommonParameters</span></span>
<span data-ttu-id="443f6-136">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="443f6-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="443f6-137">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="443f6-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="443f6-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="443f6-138">INPUTS</span></span>

### <span data-ttu-id="443f6-139">System.String</span><span class="sxs-lookup"><span data-stu-id="443f6-139">System.String</span></span>

### <span data-ttu-id="443f6-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="443f6-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="443f6-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="443f6-141">OUTPUTS</span></span>

### <span data-ttu-id="443f6-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntimeKeys</span><span class="sxs-lookup"><span data-stu-id="443f6-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntimeKeys</span></span>

## <span data-ttu-id="443f6-143">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="443f6-143">NOTES</span></span>

## <span data-ttu-id="443f6-144">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="443f6-144">RELATED LINKS</span></span>

[<span data-ttu-id="443f6-145">Get-AzDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="443f6-145">Get-AzDataFactoryV2IntegrationRuntimeKey</span></span>]()
