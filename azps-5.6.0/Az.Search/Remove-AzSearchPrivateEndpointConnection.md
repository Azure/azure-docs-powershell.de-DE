---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/powershell/module/az.search/remove-azsearchprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Remove-AzSearchPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Remove-AzSearchPrivateEndpointConnection.md
ms.openlocfilehash: 98b5f30bfe3a829d276c435c9beef71cf8a2f7de
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101936091"
---
# <span data-ttu-id="28523-101">Remove-AzSearchPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="28523-101">Remove-AzSearchPrivateEndpointConnection</span></span>

## <span data-ttu-id="28523-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="28523-102">SYNOPSIS</span></span>
<span data-ttu-id="28523-103">Entfernen Sie die private Endpunktverbindung aus dem Azure Cognitive Search-Dienst.</span><span class="sxs-lookup"><span data-stu-id="28523-103">Remove the private endpoint connection from the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="28523-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="28523-104">SYNTAX</span></span>

### <span data-ttu-id="28523-105">ResourceNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="28523-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzSearchPrivateEndpointConnection [-ResourceGroupName] <String> [-ServiceName] <String> [-Name] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="28523-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="28523-106">ParentObjectParameterSet</span></span>
```
Remove-AzSearchPrivateEndpointConnection -ParentObject <PSSearchService> [-Name] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="28523-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="28523-107">InputObjectParameterSet</span></span>
```
Remove-AzSearchPrivateEndpointConnection -InputObject <PSPrivateEndpointConnection> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="28523-108">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="28523-108">ResourceIdParameterSet</span></span>
```
Remove-AzSearchPrivateEndpointConnection [-ResourceId] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="28523-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="28523-109">DESCRIPTION</span></span>
<span data-ttu-id="28523-110">Die **Remove-AzSearchPrivateEndpointConnection** entfernt die private Endpunktverbindung aus dem Azure Cognitive Search-Dienst.</span><span class="sxs-lookup"><span data-stu-id="28523-110">The **Remove-AzSearchPrivateEndpointConnection** removes the private endpoint connection from the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="28523-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="28523-111">EXAMPLES</span></span>

### <span data-ttu-id="28523-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="28523-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSearchPrivateEndpointConnection -ResourceGroupName arjagann -ServiceName arjagann-test-cuseuap -Name arjagann-test-cuseuap-pe.4c74dd7c-7016-42ac-827a-8d5d1378f266
```

<span data-ttu-id="28523-113">In diesem Beispiel wird eine private Endpunktverbindung nach Name aus dem Suchdienst entfernt.</span><span class="sxs-lookup"><span data-stu-id="28523-113">This example removes a private endpoint connection from the search service by name.</span></span>

## <span data-ttu-id="28523-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="28523-114">PARAMETERS</span></span>

### <span data-ttu-id="28523-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28523-115">-DefaultProfile</span></span>
<span data-ttu-id="28523-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="28523-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="28523-117">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="28523-117">-Force</span></span>
<span data-ttu-id="28523-118">Bitten Sie nicht um Bestätigung.</span><span class="sxs-lookup"><span data-stu-id="28523-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="28523-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="28523-119">-InputObject</span></span>
<span data-ttu-id="28523-120">Eingabeobjekt für private Endpunktverbindung</span><span class="sxs-lookup"><span data-stu-id="28523-120">Private endpoint connection input object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSPrivateEndpointConnection
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="28523-121">-Name</span><span class="sxs-lookup"><span data-stu-id="28523-121">-Name</span></span>
<span data-ttu-id="28523-122">Name der privaten Azure Cognitive Search Service-Verbindung</span><span class="sxs-lookup"><span data-stu-id="28523-122">Azure Cognitive Search Service private endpoint connection name</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet, ParentObjectParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28523-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="28523-123">-ParentObject</span></span>
<span data-ttu-id="28523-124">Azure Cognitive Search Service Input Object.</span><span class="sxs-lookup"><span data-stu-id="28523-124">Azure Cognitive Search Service Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSSearchService
Parameter Sets: ParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="28523-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="28523-125">-PassThru</span></span>
<span data-ttu-id="28523-126">Dieses Cmdlet gibt standardmäßig kein -Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="28523-126">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="28523-127">Wenn dieser Schalter angegeben ist, gibt er "true" zurück, wenn er erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="28523-127">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="28523-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28523-128">-ResourceGroupName</span></span>
<span data-ttu-id="28523-129">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="28523-129">Resource Group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28523-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="28523-130">-ResourceId</span></span>
<span data-ttu-id="28523-131">Private Link Service Resource ID</span><span class="sxs-lookup"><span data-stu-id="28523-131">Private link service resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28523-132">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="28523-132">-ServiceName</span></span>
<span data-ttu-id="28523-133">Name des Azure Cognitive Search Service.</span><span class="sxs-lookup"><span data-stu-id="28523-133">Azure Cognitive Search Service name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28523-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="28523-134">-Confirm</span></span>
<span data-ttu-id="28523-135">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="28523-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="28523-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="28523-136">-WhatIf</span></span>
<span data-ttu-id="28523-137">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="28523-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="28523-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="28523-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="28523-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28523-139">CommonParameters</span></span>
<span data-ttu-id="28523-140">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28523-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28523-141">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="28523-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28523-142">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="28523-142">INPUTS</span></span>

### <span data-ttu-id="28523-143">Keine</span><span class="sxs-lookup"><span data-stu-id="28523-143">None</span></span>

## <span data-ttu-id="28523-144">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="28523-144">OUTPUTS</span></span>

### <span data-ttu-id="28523-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="28523-145">System.Boolean</span></span>

## <span data-ttu-id="28523-146">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="28523-146">NOTES</span></span>

## <span data-ttu-id="28523-147">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="28523-147">RELATED LINKS</span></span>

[<span data-ttu-id="28523-148">Get-AzSearchPrivateEndpointConnection.md</span><span class="sxs-lookup"><span data-stu-id="28523-148">Get-AzSearchPrivateEndpointConnection.md</span></span>](./Get-AzSearchPrivateEndpointConnection.md)

[<span data-ttu-id="28523-149">Set-AzSearchPrivateEndpointConnection.md</span><span class="sxs-lookup"><span data-stu-id="28523-149">Set-AzSearchPrivateEndpointConnection.md</span></span>](./Set-AzSearchPrivateEndpointConnection.md)