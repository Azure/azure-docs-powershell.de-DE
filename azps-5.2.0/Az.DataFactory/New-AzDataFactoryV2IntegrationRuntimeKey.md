---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/new-azdatafactoryv2integrationruntimekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryV2IntegrationRuntimeKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryV2IntegrationRuntimeKey.md
ms.openlocfilehash: 07cb597f5ca3793e3eb8db3fe153fafaa94f3501
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98290362"
---
# <span data-ttu-id="cd00a-101">New-AzDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="cd00a-101">New-AzDataFactoryV2IntegrationRuntimeKey</span></span>

## <span data-ttu-id="cd00a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cd00a-102">SYNOPSIS</span></span>
<span data-ttu-id="cd00a-103">Regenerieren Sie den selbst gehosteten Integrations-Runtime-Schlüssel erneut.</span><span class="sxs-lookup"><span data-stu-id="cd00a-103">Regenerate self-hosted integration runtime key.</span></span>

## <span data-ttu-id="cd00a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cd00a-104">SYNTAX</span></span>

### <span data-ttu-id="cd00a-105">ByIntegrationRuntimeName (Standard)</span><span class="sxs-lookup"><span data-stu-id="cd00a-105">ByIntegrationRuntimeName (Default)</span></span>
```
New-AzDataFactoryV2IntegrationRuntimeKey -KeyName <String> [-Force] [-Name] <String>
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cd00a-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="cd00a-106">ByResourceId</span></span>
```
New-AzDataFactoryV2IntegrationRuntimeKey -KeyName <String> [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cd00a-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="cd00a-107">ByIntegrationRuntimeObject</span></span>
```
New-AzDataFactoryV2IntegrationRuntimeKey -KeyName <String> [-Force] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cd00a-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cd00a-108">DESCRIPTION</span></span>
<span data-ttu-id="cd00a-109">Das Cmdlet **"New-AzDataFactoryV2IntegrationRuntimeKey"** generiert den Integrations-Runtime-Schlüssel erneut mit dem Schlüsselnamen, der durch den Parameter "KeyName" angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="cd00a-109">The cmdlet **New-AzDataFactoryV2IntegrationRuntimeKey** regenerates the integration runtime key with the key name specified by 'KeyName' parameter.</span></span> <span data-ttu-id="cd00a-110">Der vorherige Schlüssel ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="cd00a-110">The previous key will is invalid.</span></span>

## <span data-ttu-id="cd00a-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="cd00a-111">EXAMPLES</span></span>

### <span data-ttu-id="cd00a-112">Beispiel 1: Generieren eines neuen Schlüssels für eine Integrationslaufzeit</span><span class="sxs-lookup"><span data-stu-id="cd00a-112">Example 1: Generate a new key for an integration runtime</span></span>
```
PS C:\> New-AzDataFactoryV2IntegrationRuntimeKey -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' -KeyName authKey2

AuthKey1 AuthKey2
-------- --------
         IR@89895504-f647-48fd-8dd3-42fa556d67e3@***
```

<span data-ttu-id="cd00a-113">Das Cmdlet generiert den Schlüssel "authKey2" für die Integrationslaufzeit mit dem Namen "test-selfhost-ir".</span><span class="sxs-lookup"><span data-stu-id="cd00a-113">The cmdlet regenerates key 'authKey2' for integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="cd00a-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cd00a-114">PARAMETERS</span></span>

### <span data-ttu-id="cd00a-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="cd00a-115">-DataFactoryName</span></span>
<span data-ttu-id="cd00a-116">Der Name der Daten factory.</span><span class="sxs-lookup"><span data-stu-id="cd00a-116">The data factory name.</span></span>

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

### <span data-ttu-id="cd00a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd00a-117">-DefaultProfile</span></span>
<span data-ttu-id="cd00a-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="cd00a-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cd00a-119">-Force</span><span class="sxs-lookup"><span data-stu-id="cd00a-119">-Force</span></span>
<span data-ttu-id="cd00a-120">Führt das Cmdlet ohne Bestätigungsaufforderung aus.</span><span class="sxs-lookup"><span data-stu-id="cd00a-120">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="cd00a-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cd00a-121">-InputObject</span></span>
<span data-ttu-id="cd00a-122">Das Integrations-Runtime-Objekt.</span><span class="sxs-lookup"><span data-stu-id="cd00a-122">The integration runtime object.</span></span>

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

### <span data-ttu-id="cd00a-123">-KeyName</span><span class="sxs-lookup"><span data-stu-id="cd00a-123">-KeyName</span></span>
<span data-ttu-id="cd00a-124">Der Name des Authentifizierungsschlüssels der selbst gehosteten Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="cd00a-124">The authentication key name of the self-hosted integration runtime.</span></span>

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

### <span data-ttu-id="cd00a-125">-Name</span><span class="sxs-lookup"><span data-stu-id="cd00a-125">-Name</span></span>
<span data-ttu-id="cd00a-126">Der Name der Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="cd00a-126">The integration runtime name.</span></span>

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

### <span data-ttu-id="cd00a-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd00a-127">-ResourceGroupName</span></span>
<span data-ttu-id="cd00a-128">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="cd00a-128">The resource group name.</span></span>

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

### <span data-ttu-id="cd00a-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cd00a-129">-ResourceId</span></span>
<span data-ttu-id="cd00a-130">Die Azure-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="cd00a-130">The Azure resource ID.</span></span>

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

### <span data-ttu-id="cd00a-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cd00a-131">-Confirm</span></span>
<span data-ttu-id="cd00a-132">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="cd00a-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd00a-133">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="cd00a-133">-WhatIf</span></span>
<span data-ttu-id="cd00a-134">Zeigt, was geschieht, wenn das Cmdlet ausgeführt, aber nicht ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="cd00a-134">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="cd00a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd00a-135">CommonParameters</span></span>
<span data-ttu-id="cd00a-136">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd00a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd00a-137">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd00a-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd00a-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="cd00a-138">INPUTS</span></span>

### <span data-ttu-id="cd00a-139">System.String</span><span class="sxs-lookup"><span data-stu-id="cd00a-139">System.String</span></span>

### <span data-ttu-id="cd00a-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="cd00a-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="cd00a-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="cd00a-141">OUTPUTS</span></span>

### <span data-ttu-id="cd00a-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntimeKeys</span><span class="sxs-lookup"><span data-stu-id="cd00a-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntimeKeys</span></span>

## <span data-ttu-id="cd00a-143">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="cd00a-143">NOTES</span></span>

## <span data-ttu-id="cd00a-144">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="cd00a-144">RELATED LINKS</span></span>

[<span data-ttu-id="cd00a-145">Get-AzDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="cd00a-145">Get-AzDataFactoryV2IntegrationRuntimeKey</span></span>]()
