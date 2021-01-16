---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/set-azeventhubgeodrconfigurationfailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubGeoDRConfigurationFailOver.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubGeoDRConfigurationFailOver.md
ms.openlocfilehash: 4ee96fbe20fca3f0af1f0bb9604f178b912d0ea2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98289361"
---
# <span data-ttu-id="ca13f-101">Set-AzEventHubGeoDRConfigurationFailOver</span><span class="sxs-lookup"><span data-stu-id="ca13f-101">Set-AzEventHubGeoDRConfigurationFailOver</span></span>

## <span data-ttu-id="ca13f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ca13f-102">SYNOPSIS</span></span>
<span data-ttu-id="ca13f-103">Ruft geo-DR-Failover auf und konfiguriert den Alias so neu, dass er auf den sekundären Namespace verweisen kann.</span><span class="sxs-lookup"><span data-stu-id="ca13f-103">Invokes GEO DR failover and reconfigure the alias to point to the secondary namespace</span></span>

## <span data-ttu-id="ca13f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ca13f-104">SYNTAX</span></span>

### <span data-ttu-id="ca13f-105">GeoDRParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="ca13f-105">GeoDRParameterSet (Default)</span></span>
```
Set-AzEventHubGeoDRConfigurationFailOver [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca13f-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="ca13f-106">GeoDRConfigurationInputObjectSet</span></span>
```
Set-AzEventHubGeoDRConfigurationFailOver [-InputObject] <PSEventHubDRConfigurationAttributes> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca13f-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ca13f-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Set-AzEventHubGeoDRConfigurationFailOver [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ca13f-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ca13f-108">DESCRIPTION</span></span>
<span data-ttu-id="ca13f-109">Das **Cmdlet "Set-AzEventHubGeoDRConfigurationFailOver"** ruft geo-DR-Failover auf und konfiguriert den Alias so neu, dass er auf den sekundären Namespace zeigt.</span><span class="sxs-lookup"><span data-stu-id="ca13f-109">The **Set-AzEventHubGeoDRConfigurationFailOver** cmdlet invokes GEO DR failover and reconfigure the alias to point to the secondary namespace</span></span>

## <span data-ttu-id="ca13f-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ca13f-110">EXAMPLES</span></span>

### <span data-ttu-id="ca13f-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ca13f-111">Example 1</span></span>
```
PS C:\>Set-AzEventHubGeoDRConfigurationFailOver -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Secondary" -Name "SampleDRConfigName"
```

<span data-ttu-id="ca13f-112">Ruft den Failover über den Alias "SampleDRConfigName" auf, konfiguriert ihn neu und zeigt auf den sekundären Namespace "SampleNamespace_Secondary"</span><span class="sxs-lookup"><span data-stu-id="ca13f-112">Invokes the Failover over alias "SampleDRConfigName", reconfigures and point to Secondary namespace "SampleNamespace_Secondary"</span></span>

## <span data-ttu-id="ca13f-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ca13f-113">PARAMETERS</span></span>

### <span data-ttu-id="ca13f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca13f-114">-DefaultProfile</span></span>
<span data-ttu-id="ca13f-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ca13f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ca13f-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ca13f-116">-InputObject</span></span>
<span data-ttu-id="ca13f-117">Eventhub GeoDR Configuration Object</span><span class="sxs-lookup"><span data-stu-id="ca13f-117">Eventhub GeoDR Configuration Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes
Parameter Sets: GeoDRConfigurationInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ca13f-118">-Name</span><span class="sxs-lookup"><span data-stu-id="ca13f-118">-Name</span></span>
<span data-ttu-id="ca13f-119">Name der DR-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="ca13f-119">DR Configuration Name</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca13f-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="ca13f-120">-Namespace</span></span>
<span data-ttu-id="ca13f-121">Namespacename – Sekundärer Namespace</span><span class="sxs-lookup"><span data-stu-id="ca13f-121">Namespace Name - Secondary Namespace</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca13f-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ca13f-122">-PassThru</span></span>
<span data-ttu-id="ca13f-123">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="ca13f-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="ca13f-124">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="ca13f-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ca13f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca13f-125">-ResourceGroupName</span></span>
<span data-ttu-id="ca13f-126">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="ca13f-126">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca13f-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ca13f-127">-ResourceId</span></span>
<span data-ttu-id="ca13f-128">GeoDRConfiguration Resource Id</span><span class="sxs-lookup"><span data-stu-id="ca13f-128">GeoDRConfiguration Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRConfigResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca13f-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ca13f-129">-Confirm</span></span>
<span data-ttu-id="ca13f-130">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ca13f-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ca13f-131">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="ca13f-131">-WhatIf</span></span>
<span data-ttu-id="ca13f-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ca13f-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ca13f-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ca13f-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ca13f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca13f-134">CommonParameters</span></span>
<span data-ttu-id="ca13f-135">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca13f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca13f-136">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ca13f-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca13f-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ca13f-137">INPUTS</span></span>

### <span data-ttu-id="ca13f-138">System.String</span><span class="sxs-lookup"><span data-stu-id="ca13f-138">System.String</span></span>

### <span data-ttu-id="ca13f-139">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="ca13f-139">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span></span>

## <span data-ttu-id="ca13f-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ca13f-140">OUTPUTS</span></span>

### <span data-ttu-id="ca13f-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ca13f-141">System.Boolean</span></span>

## <span data-ttu-id="ca13f-142">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="ca13f-142">NOTES</span></span>

## <span data-ttu-id="ca13f-143">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="ca13f-143">RELATED LINKS</span></span>
