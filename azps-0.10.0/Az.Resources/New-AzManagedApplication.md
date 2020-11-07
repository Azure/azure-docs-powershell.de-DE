---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-Azmanagedapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzManagedApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzManagedApplication.md
ms.openlocfilehash: a34754e0032f2dc8b833eb6b03de6e97ab5486fe
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843363"
---
# <span data-ttu-id="b3954-101">New-AzManagedApplication</span><span class="sxs-lookup"><span data-stu-id="b3954-101">New-AzManagedApplication</span></span>

## <span data-ttu-id="b3954-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b3954-102">SYNOPSIS</span></span>
<span data-ttu-id="b3954-103">Erstellt eine Azure-verwaltete Anwendung.</span><span class="sxs-lookup"><span data-stu-id="b3954-103">Creates an Azure managed application.</span></span>

## <span data-ttu-id="b3954-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b3954-104">SYNTAX</span></span>

```
New-AzManagedApplication -Name <String> -ResourceGroupName <String> -ManagedResourceGroupName <String>
 [-ManagedApplicationDefinitionId <String>] -Location <String> [-Parameter <String>] -Kind <ApplicationKind>
 [-Plan <Hashtable>] [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b3954-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b3954-105">DESCRIPTION</span></span>
<span data-ttu-id="b3954-106">Das Cmdlet **New-AzManagedApplication** erstellt eine Azure-verwaltete Anwendung.</span><span class="sxs-lookup"><span data-stu-id="b3954-106">The **New-AzManagedApplication** cmdlet creates an Azure Managed Application.</span></span>

## <span data-ttu-id="b3954-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b3954-107">EXAMPLES</span></span>

### <span data-ttu-id="b3954-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b3954-108">Example 1</span></span>
```
PS C:\>New-AzManagedApplication -Name "myManagedApplication" -ResourceGroupName myRG -ManagedResourceGroupName myManagedRG -ManagedApplicationDefinitionId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/providers/Microsoft.Solutions/applicationDefinitions/myAppDef" -Location eastus2euap -Kind ServiceCatalog
```

<span data-ttu-id="b3954-109">Mit diesem Befehl wird eine verwaltete Anwendung erstellt</span><span class="sxs-lookup"><span data-stu-id="b3954-109">This command creates a managed application</span></span>

## <span data-ttu-id="b3954-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="b3954-110">PARAMETERS</span></span>

### <span data-ttu-id="b3954-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="b3954-111">-ApiVersion</span></span>
<span data-ttu-id="b3954-112">Gibt an, dass die Version der zu verwendenden Ressourcenanbieter-API verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b3954-112">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="b3954-113">Wenn Sie nicht angegeben wird, wird die API-Version automatisch als die neueste verfügbare Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="b3954-113">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="b3954-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3954-114">-DefaultProfile</span></span>
<span data-ttu-id="b3954-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b3954-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3954-116">-Art</span><span class="sxs-lookup"><span data-stu-id="b3954-116">-Kind</span></span>
<span data-ttu-id="b3954-117">Die Art der verwalteten Anwendung.</span><span class="sxs-lookup"><span data-stu-id="b3954-117">The managed application kind.</span></span>
<span data-ttu-id="b3954-118">Eine der Marketplace-oder servicecatalog</span><span class="sxs-lookup"><span data-stu-id="b3954-118">One of marketplace or servicecatalog</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Application.ApplicationKind
Parameter Sets: (All)
Aliases:
Accepted values: ServiceCatalog, MarketPlace

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3954-119">-Standort</span><span class="sxs-lookup"><span data-stu-id="b3954-119">-Location</span></span>
<span data-ttu-id="b3954-120">Der Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="b3954-120">The resource location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3954-121">-ManagedApplicationDefinitionId</span><span class="sxs-lookup"><span data-stu-id="b3954-121">-ManagedApplicationDefinitionId</span></span>
<span data-ttu-id="b3954-122">Der Name der verwalteten Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="b3954-122">The managed resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3954-123">-ManagedResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3954-123">-ManagedResourceGroupName</span></span>
<span data-ttu-id="b3954-124">Der Name der verwalteten Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="b3954-124">The managed resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3954-125">-Name</span><span class="sxs-lookup"><span data-stu-id="b3954-125">-Name</span></span>
<span data-ttu-id="b3954-126">Der Name der verwalteten Anwendung.</span><span class="sxs-lookup"><span data-stu-id="b3954-126">The managed application name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3954-127">-Parameter</span><span class="sxs-lookup"><span data-stu-id="b3954-127">-Parameter</span></span>
<span data-ttu-id="b3954-128">Die JSON-formatierte Zeichenfolge von Parametern für verwaltete Anwendung.</span><span class="sxs-lookup"><span data-stu-id="b3954-128">The JSON formatted string of parameters for managed application.</span></span>
<span data-ttu-id="b3954-129">Dies kann entweder ein Pfad zu einem Dateinamen oder URI sein, der die Parameter enthält, oder die Parameter als Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="b3954-129">This can either be a path to a file name or uri containing the parameters, or the parameters as string.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3954-130">-Plan</span><span class="sxs-lookup"><span data-stu-id="b3954-130">-Plan</span></span>
<span data-ttu-id="b3954-131">Eine Hashtabelle, die verwaltete Anwendungsplan Eigenschaften darstellt.</span><span class="sxs-lookup"><span data-stu-id="b3954-131">A hash table which represents managed application plan properties.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: PlanObject

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3954-132">-Pre</span><span class="sxs-lookup"><span data-stu-id="b3954-132">-Pre</span></span>
<span data-ttu-id="b3954-133">Wenn festgelegt, gibt an, dass das Cmdlet Vorabversion-API-Versionen verwenden soll, wenn die zu verwendende Version automatisch ermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="b3954-133">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="b3954-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3954-134">-ResourceGroupName</span></span>
<span data-ttu-id="b3954-135">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="b3954-135">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3954-136">-Tag</span><span class="sxs-lookup"><span data-stu-id="b3954-136">-Tag</span></span>
<span data-ttu-id="b3954-137">Eine Hashtable, die Ressourcen Tags darstellt.</span><span class="sxs-lookup"><span data-stu-id="b3954-137">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3954-138">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b3954-138">-Confirm</span></span>
<span data-ttu-id="b3954-139">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b3954-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b3954-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3954-140">-WhatIf</span></span>
<span data-ttu-id="b3954-141">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b3954-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b3954-142">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b3954-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b3954-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3954-143">CommonParameters</span></span>
<span data-ttu-id="b3954-144">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3954-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3954-145">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b3954-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3954-146">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b3954-146">INPUTS</span></span>

### <span data-ttu-id="b3954-147">System. String</span><span class="sxs-lookup"><span data-stu-id="b3954-147">System.String</span></span>

### <span data-ttu-id="b3954-148">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="b3954-148">System.Collections.Hashtable</span></span>

## <span data-ttu-id="b3954-149">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b3954-149">OUTPUTS</span></span>

### <span data-ttu-id="b3954-150">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="b3954-150">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="b3954-151">Notizen</span><span class="sxs-lookup"><span data-stu-id="b3954-151">NOTES</span></span>

## <span data-ttu-id="b3954-152">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b3954-152">RELATED LINKS</span></span>
