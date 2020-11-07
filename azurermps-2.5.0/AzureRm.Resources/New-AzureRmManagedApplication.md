---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermmanagedapplication
schema: 2.0.0
ms.openlocfilehash: 49b8351109289c46ce57224aa47b1675abe54841
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850283"
---
# <span data-ttu-id="be300-101">New-AzureRmManagedApplication</span><span class="sxs-lookup"><span data-stu-id="be300-101">New-AzureRmManagedApplication</span></span>

## <span data-ttu-id="be300-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="be300-102">SYNOPSIS</span></span>
<span data-ttu-id="be300-103">Erstellt eine Azure-verwaltete Anwendung.</span><span class="sxs-lookup"><span data-stu-id="be300-103">Creates an Azure managed application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="be300-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="be300-104">SYNTAX</span></span>

```
New-AzureRmManagedApplication -Name <String> -ResourceGroupName <String> -ManagedResourceGroupName <String>
 [-ManagedApplicationDefinitionId <String>] -Location <String> [-Parameter <String>] -Kind <ApplicationKind>
 [-Plan <Hashtable>] [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="be300-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="be300-105">DESCRIPTION</span></span>
<span data-ttu-id="be300-106">Das Cmdlet **New-AzureRmManagedApplication** erstellt eine Azure-verwaltete Anwendung.</span><span class="sxs-lookup"><span data-stu-id="be300-106">The **New-AzureRmManagedApplication** cmdlet creates an Azure Managed Application.</span></span>

## <span data-ttu-id="be300-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="be300-107">EXAMPLES</span></span>

### <span data-ttu-id="be300-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="be300-108">Example 1</span></span>
```
PS C:\>New-AzureRmManagedApplication -Name "myManagedApplication" -ResourceGroupName myRG -ManagedResourceGroupName myManagedRG -ManagedApplicationDefinitionId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/providers/Microsoft.Solutions/applicationDefinitions/myAppDef" -Location eastus2euap -Kind ServiceCatalog
```

<span data-ttu-id="be300-109">Mit diesem Befehl wird eine verwaltete Anwendung erstellt</span><span class="sxs-lookup"><span data-stu-id="be300-109">This command creates a managed application</span></span>

## <span data-ttu-id="be300-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="be300-110">PARAMETERS</span></span>

### <span data-ttu-id="be300-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="be300-111">-ApiVersion</span></span>
<span data-ttu-id="be300-112">Gibt an, dass die Version der zu verwendenden Ressourcenanbieter-API verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="be300-112">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="be300-113">Wenn Sie nicht angegeben wird, wird die API-Version automatisch als die neueste verfügbare Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="be300-113">If not specified, the API version is automatically determined as the latest available.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be300-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be300-114">-DefaultProfile</span></span>
<span data-ttu-id="be300-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="be300-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="be300-116">-Art</span><span class="sxs-lookup"><span data-stu-id="be300-116">-Kind</span></span>
<span data-ttu-id="be300-117">Die Art der verwalteten Anwendung.</span><span class="sxs-lookup"><span data-stu-id="be300-117">The managed application kind.</span></span>
<span data-ttu-id="be300-118">Eine der Marketplace-oder servicecatalog</span><span class="sxs-lookup"><span data-stu-id="be300-118">One of marketplace or servicecatalog</span></span>

```yaml
Type: ApplicationKind
Parameter Sets: (All)
Aliases:
Accepted values: ServiceCatalog, MarketPlace

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be300-119">-Standort</span><span class="sxs-lookup"><span data-stu-id="be300-119">-Location</span></span>
<span data-ttu-id="be300-120">Der Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="be300-120">The resource location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be300-121">-ManagedApplicationDefinitionId</span><span class="sxs-lookup"><span data-stu-id="be300-121">-ManagedApplicationDefinitionId</span></span>
<span data-ttu-id="be300-122">Der Name der verwalteten Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="be300-122">The managed resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be300-123">-ManagedResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be300-123">-ManagedResourceGroupName</span></span>
<span data-ttu-id="be300-124">Der Name der verwalteten Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="be300-124">The managed resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be300-125">-Name</span><span class="sxs-lookup"><span data-stu-id="be300-125">-Name</span></span>
<span data-ttu-id="be300-126">Der Name der verwalteten Anwendung.</span><span class="sxs-lookup"><span data-stu-id="be300-126">The managed application name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be300-127">-Parameter</span><span class="sxs-lookup"><span data-stu-id="be300-127">-Parameter</span></span>
<span data-ttu-id="be300-128">Die JSON-formatierte Zeichenfolge von Parametern für verwaltete Anwendung.</span><span class="sxs-lookup"><span data-stu-id="be300-128">The JSON formatted string of parameters for managed application.</span></span>
<span data-ttu-id="be300-129">Dies kann entweder ein Pfad zu einem Dateinamen oder URI sein, der die Parameter enthält, oder die Parameter als Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="be300-129">This can either be a path to a file name or uri containing the parameters, or the parameters as string.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be300-130">-Plan</span><span class="sxs-lookup"><span data-stu-id="be300-130">-Plan</span></span>
<span data-ttu-id="be300-131">Eine Hashtabelle, die verwaltete Anwendungsplan Eigenschaften darstellt.</span><span class="sxs-lookup"><span data-stu-id="be300-131">A hash table which represents managed application plan properties.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: PlanObject

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be300-132">-Pre</span><span class="sxs-lookup"><span data-stu-id="be300-132">-Pre</span></span>
<span data-ttu-id="be300-133">Wenn festgelegt, gibt an, dass das Cmdlet Vorabversion-API-Versionen verwenden soll, wenn die zu verwendende Version automatisch ermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="be300-133">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="be300-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be300-134">-ResourceGroupName</span></span>
<span data-ttu-id="be300-135">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="be300-135">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be300-136">-Tag</span><span class="sxs-lookup"><span data-stu-id="be300-136">-Tag</span></span>
<span data-ttu-id="be300-137">Eine Hashtable, die Ressourcen Tags darstellt.</span><span class="sxs-lookup"><span data-stu-id="be300-137">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be300-138">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="be300-138">-Confirm</span></span>
<span data-ttu-id="be300-139">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="be300-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="be300-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="be300-140">-WhatIf</span></span>
<span data-ttu-id="be300-141">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="be300-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="be300-142">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="be300-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="be300-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be300-143">CommonParameters</span></span>
<span data-ttu-id="be300-144">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="be300-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be300-145">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="be300-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be300-146">Eingaben</span><span class="sxs-lookup"><span data-stu-id="be300-146">INPUTS</span></span>

### <span data-ttu-id="be300-147">System. String</span><span class="sxs-lookup"><span data-stu-id="be300-147">System.String</span></span>
<span data-ttu-id="be300-148">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="be300-148">System.Collections.Hashtable</span></span>

## <span data-ttu-id="be300-149">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="be300-149">OUTPUTS</span></span>

### <span data-ttu-id="be300-150">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="be300-150">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="be300-151">Notizen</span><span class="sxs-lookup"><span data-stu-id="be300-151">NOTES</span></span>

## <span data-ttu-id="be300-152">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="be300-152">RELATED LINKS</span></span>
