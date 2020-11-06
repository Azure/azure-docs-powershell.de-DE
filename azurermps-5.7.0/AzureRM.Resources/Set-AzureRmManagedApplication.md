---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/set-azurermmanagedapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmManagedApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmManagedApplication.md
ms.openlocfilehash: 870769c6bb2557b2a654b4625d3f2c7ea1b4293e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93480937"
---
# <span data-ttu-id="de60d-101">Set-AzureRmManagedApplication</span><span class="sxs-lookup"><span data-stu-id="de60d-101">Set-AzureRmManagedApplication</span></span>

## <span data-ttu-id="de60d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="de60d-102">SYNOPSIS</span></span>
<span data-ttu-id="de60d-103">Verwaltete Anwendung für Updates</span><span class="sxs-lookup"><span data-stu-id="de60d-103">Updates managed application</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="de60d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="de60d-104">SYNTAX</span></span>

### <span data-ttu-id="de60d-105">SetByNameAndResourceGroup (Standard)</span><span class="sxs-lookup"><span data-stu-id="de60d-105">SetByNameAndResourceGroup (Default)</span></span>
```
Set-AzureRmManagedApplication -Name <String> -ResourceGroupName <String> [-ManagedResourceGroupName <String>]
 [-ManagedApplicationDefinitionId <String>] [-Parameter <String>] [-Kind <String>] [-Plan <Hashtable>]
 [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="de60d-106">SetById</span><span class="sxs-lookup"><span data-stu-id="de60d-106">SetById</span></span>
```
Set-AzureRmManagedApplication -Id <String> [-ManagedResourceGroupName <String>]
 [-ManagedApplicationDefinitionId <String>] [-Parameter <String>] [-Kind <String>] [-Plan <Hashtable>]
 [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="de60d-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="de60d-107">DESCRIPTION</span></span>
<span data-ttu-id="de60d-108">Das Cmdlet " **Satz-AzureRmManagedApplication** " aktualisiert verwaltete Anwendungen</span><span class="sxs-lookup"><span data-stu-id="de60d-108">The **Set-AzureRmManagedApplication** cmdlet updates managed applications</span></span>

## <span data-ttu-id="de60d-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="de60d-109">EXAMPLES</span></span>

### <span data-ttu-id="de60d-110">Beispiel 1: Aktualisieren der Definitionsbeschreibung für verwaltete Anwendungen</span><span class="sxs-lookup"><span data-stu-id="de60d-110">Example 1: Update managed application definition description</span></span>
```
PS C:\>Set-AzureRmManagedApplication -ResourceId "/subscriptions/mySubId/resourcegroups/myRG/Microsoft.Solutions/applications/myApp" -Description "Updated description here"
```

<span data-ttu-id="de60d-111">Mit diesem Befehl wird die Beschreibung der verwalteten Anwendung aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="de60d-111">This command updates the managed application description</span></span>

## <span data-ttu-id="de60d-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="de60d-112">PARAMETERS</span></span>

### <span data-ttu-id="de60d-113">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="de60d-113">-ApiVersion</span></span>
<span data-ttu-id="de60d-114">Gibt an, dass die Version der zu verwendenden Ressourcenanbieter-API verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="de60d-114">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="de60d-115">Wenn Sie nicht angegeben wird, wird die API-Version automatisch als die neueste verfügbare Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="de60d-115">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="de60d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de60d-116">-DefaultProfile</span></span>
<span data-ttu-id="de60d-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="de60d-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="de60d-118">-ID</span><span class="sxs-lookup"><span data-stu-id="de60d-118">-Id</span></span>
<span data-ttu-id="de60d-119">Die vollqualifizierte verwaltete Anwendungs-ID, einschließlich des Abonnements.</span><span class="sxs-lookup"><span data-stu-id="de60d-119">The fully qualified managed application Id, including the subscription.</span></span> <span data-ttu-id="de60d-120">z.b./Subscriptions/{SubscriptionId}/ResourceGroups/{resourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de60d-120">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName</span></span>

```yaml
Type: String
Parameter Sets: SetById
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de60d-121">-Art</span><span class="sxs-lookup"><span data-stu-id="de60d-121">-Kind</span></span>
<span data-ttu-id="de60d-122">Die Art der verwalteten Anwendung.</span><span class="sxs-lookup"><span data-stu-id="de60d-122">The managed application kind.</span></span>
<span data-ttu-id="de60d-123">Eine der Marketplace-oder servicecatalog</span><span class="sxs-lookup"><span data-stu-id="de60d-123">One of marketplace or servicecatalog</span></span>

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

### <span data-ttu-id="de60d-124">-ManagedApplicationDefinitionId</span><span class="sxs-lookup"><span data-stu-id="de60d-124">-ManagedApplicationDefinitionId</span></span>
<span data-ttu-id="de60d-125">Der Name der verwalteten Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="de60d-125">The managed resource group name.</span></span>

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

### <span data-ttu-id="de60d-126">-ManagedResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de60d-126">-ManagedResourceGroupName</span></span>
<span data-ttu-id="de60d-127">Der Name der verwalteten Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="de60d-127">The managed resource group name.</span></span>

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

### <span data-ttu-id="de60d-128">-Name</span><span class="sxs-lookup"><span data-stu-id="de60d-128">-Name</span></span>
<span data-ttu-id="de60d-129">Der Name der verwalteten Anwendung.</span><span class="sxs-lookup"><span data-stu-id="de60d-129">The managed application name.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de60d-130">-Parameter</span><span class="sxs-lookup"><span data-stu-id="de60d-130">-Parameter</span></span>
<span data-ttu-id="de60d-131">Die JSON-formatierte Zeichenfolge von Parametern für verwaltete Anwendung.</span><span class="sxs-lookup"><span data-stu-id="de60d-131">The JSON formatted string of parameters for managed application.</span></span>
<span data-ttu-id="de60d-132">Dies kann entweder ein Pfad zu einem Dateinamen oder URI sein, der die Parameter enthält, oder die Parameter als Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="de60d-132">This can either be a path to a file name or uri containing the parameters, or the parameters as string.</span></span>

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

### <span data-ttu-id="de60d-133">-Plan</span><span class="sxs-lookup"><span data-stu-id="de60d-133">-Plan</span></span>
<span data-ttu-id="de60d-134">Eine Hashtabelle, die verwaltete Anwendungsplan Eigenschaften darstellt.</span><span class="sxs-lookup"><span data-stu-id="de60d-134">A hash table which represents managed application plan properties.</span></span>

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

### <span data-ttu-id="de60d-135">-Pre</span><span class="sxs-lookup"><span data-stu-id="de60d-135">-Pre</span></span>
<span data-ttu-id="de60d-136">Wenn festgelegt, gibt an, dass das Cmdlet Vorabversion-API-Versionen verwenden soll, wenn die zu verwendende Version automatisch ermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="de60d-136">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="de60d-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de60d-137">-ResourceGroupName</span></span>
<span data-ttu-id="de60d-138">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="de60d-138">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de60d-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="de60d-139">-Tag</span></span>
<span data-ttu-id="de60d-140">Eine Hashtabelle, die Ressourcenkategorien darstellt.</span><span class="sxs-lookup"><span data-stu-id="de60d-140">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="de60d-141">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="de60d-141">-Confirm</span></span>
<span data-ttu-id="de60d-142">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="de60d-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="de60d-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="de60d-143">-WhatIf</span></span>
<span data-ttu-id="de60d-144">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="de60d-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="de60d-145">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="de60d-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="de60d-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de60d-146">CommonParameters</span></span>
<span data-ttu-id="de60d-147">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de60d-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de60d-148">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de60d-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de60d-149">Eingaben</span><span class="sxs-lookup"><span data-stu-id="de60d-149">INPUTS</span></span>

### <span data-ttu-id="de60d-150">System. String</span><span class="sxs-lookup"><span data-stu-id="de60d-150">System.String</span></span>
<span data-ttu-id="de60d-151">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="de60d-151">System.Collections.Hashtable</span></span>

## <span data-ttu-id="de60d-152">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="de60d-152">OUTPUTS</span></span>

### <span data-ttu-id="de60d-153">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="de60d-153">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="de60d-154">Notizen</span><span class="sxs-lookup"><span data-stu-id="de60d-154">NOTES</span></span>

## <span data-ttu-id="de60d-155">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="de60d-155">RELATED LINKS</span></span>
