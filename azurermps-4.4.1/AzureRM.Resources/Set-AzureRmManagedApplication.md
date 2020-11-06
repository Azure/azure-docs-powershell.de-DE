---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmManagedApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmManagedApplication.md
ms.openlocfilehash: 2a242f7a265efa2dd97f967101074615381d4cd5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93481609"
---
# <span data-ttu-id="0b21b-101">Set-AzureRmManagedApplication</span><span class="sxs-lookup"><span data-stu-id="0b21b-101">Set-AzureRmManagedApplication</span></span>

## <span data-ttu-id="0b21b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0b21b-102">SYNOPSIS</span></span>
<span data-ttu-id="0b21b-103">Verwaltete Anwendung für Updates</span><span class="sxs-lookup"><span data-stu-id="0b21b-103">Updates managed application</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0b21b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0b21b-104">SYNTAX</span></span>

### <span data-ttu-id="0b21b-105">Der Parametersatz für verwaltete Anwendungsnamen.</span><span class="sxs-lookup"><span data-stu-id="0b21b-105">The managed application name parameter set.</span></span> <span data-ttu-id="0b21b-106">Standard</span><span class="sxs-lookup"><span data-stu-id="0b21b-106">(Default)</span></span>
```
Set-AzureRmManagedApplication -Name <String> -ResourceGroupName <String> [-ManagedResourceGroupName <String>]
 [-ManagedApplicationDefinitionId <String>] [-Parameter <String>] [-Kind <String>] [-Plan <Hashtable>]
 [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0b21b-107">Der Parametersatz der verwalteten Anwendungs-ID.</span><span class="sxs-lookup"><span data-stu-id="0b21b-107">The managed application Id parameter set.</span></span>
```
Set-AzureRmManagedApplication -Id <String> [-ManagedResourceGroupName <String>]
 [-ManagedApplicationDefinitionId <String>] [-Parameter <String>] [-Kind <String>] [-Plan <Hashtable>]
 [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0b21b-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0b21b-108">DESCRIPTION</span></span>
<span data-ttu-id="0b21b-109">Das Cmdlet " **Satz-AzureRmManagedApplication** " aktualisiert verwaltete Anwendungen</span><span class="sxs-lookup"><span data-stu-id="0b21b-109">The **Set-AzureRmManagedApplication** cmdlet updates managed applications</span></span>

## <span data-ttu-id="0b21b-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0b21b-110">EXAMPLES</span></span>

### <span data-ttu-id="0b21b-111">Beispiel 1: Aktualisieren der Definitionsbeschreibung für verwaltete Anwendungen</span><span class="sxs-lookup"><span data-stu-id="0b21b-111">Example 1: Update managed application definition description</span></span>
```
PS C:\>Set-AzureRmManagedApplication -ResourceId "/subscriptions/mySubId/resourcegroups/myRG/Microsoft.Solutions/applications/myApp" -Description "Updated description here"
```

<span data-ttu-id="0b21b-112">Mit diesem Befehl wird die Beschreibung der verwalteten Anwendung aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="0b21b-112">This command updates the managed application description</span></span>

## <span data-ttu-id="0b21b-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="0b21b-113">PARAMETERS</span></span>

### <span data-ttu-id="0b21b-114">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="0b21b-114">-ApiVersion</span></span>
<span data-ttu-id="0b21b-115">Gibt an, dass die Version der zu verwendenden Ressourcenanbieter-API verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="0b21b-115">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="0b21b-116">Wenn Sie nicht angegeben wird, wird die API-Version automatisch als die neueste verfügbare Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="0b21b-116">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="0b21b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b21b-117">-DefaultProfile</span></span>
<span data-ttu-id="0b21b-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0b21b-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b21b-119">-Art</span><span class="sxs-lookup"><span data-stu-id="0b21b-119">-Kind</span></span>
<span data-ttu-id="0b21b-120">Die Art der verwalteten Anwendung.</span><span class="sxs-lookup"><span data-stu-id="0b21b-120">The managed application kind.</span></span>
<span data-ttu-id="0b21b-121">Eine der Marketplace-oder servicecatalog</span><span class="sxs-lookup"><span data-stu-id="0b21b-121">One of marketplace or servicecatalog</span></span>

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

### <span data-ttu-id="0b21b-122">-ManagedApplicationDefinitionId</span><span class="sxs-lookup"><span data-stu-id="0b21b-122">-ManagedApplicationDefinitionId</span></span>
<span data-ttu-id="0b21b-123">Der Name der verwalteten Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="0b21b-123">The managed resource group name.</span></span>

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

### <span data-ttu-id="0b21b-124">-ManagedResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b21b-124">-ManagedResourceGroupName</span></span>
<span data-ttu-id="0b21b-125">Der Name der verwalteten Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="0b21b-125">The managed resource group name.</span></span>

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

### <span data-ttu-id="0b21b-126">-Name</span><span class="sxs-lookup"><span data-stu-id="0b21b-126">-Name</span></span>
<span data-ttu-id="0b21b-127">Der Name der verwalteten Anwendung.</span><span class="sxs-lookup"><span data-stu-id="0b21b-127">The managed application name.</span></span>

```yaml
Type: System.String
Parameter Sets: The managed application name parameter set.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b21b-128">-Parameter</span><span class="sxs-lookup"><span data-stu-id="0b21b-128">-Parameter</span></span>
<span data-ttu-id="0b21b-129">Die JSON-formatierte Zeichenfolge von Parametern für verwaltete Anwendung.</span><span class="sxs-lookup"><span data-stu-id="0b21b-129">The JSON formatted string of parameters for managed application.</span></span>
<span data-ttu-id="0b21b-130">Dies kann entweder ein Pfad zu einem Dateinamen oder URI sein, der die Parameter enthält, oder die Parameter als Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="0b21b-130">This can either be a path to a file name or uri containing the parameters, or the parameters as string.</span></span>

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

### <span data-ttu-id="0b21b-131">-Plan</span><span class="sxs-lookup"><span data-stu-id="0b21b-131">-Plan</span></span>
<span data-ttu-id="0b21b-132">Eine Hashtabelle, die verwaltete Anwendungsplan Eigenschaften darstellt.</span><span class="sxs-lookup"><span data-stu-id="0b21b-132">A hash table which represents managed application plan properties.</span></span>

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

### <span data-ttu-id="0b21b-133">-Pre</span><span class="sxs-lookup"><span data-stu-id="0b21b-133">-Pre</span></span>
<span data-ttu-id="0b21b-134">Wenn festgelegt, gibt an, dass das Cmdlet Vorabversion-API-Versionen verwenden soll, wenn die zu verwendende Version automatisch ermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="0b21b-134">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="0b21b-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b21b-135">-ResourceGroupName</span></span>
<span data-ttu-id="0b21b-136">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="0b21b-136">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: The managed application name parameter set.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b21b-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="0b21b-137">-Tag</span></span>
<span data-ttu-id="0b21b-138">Eine Hashtabelle, die Ressourcenkategorien darstellt.</span><span class="sxs-lookup"><span data-stu-id="0b21b-138">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="0b21b-139">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="0b21b-139">-Confirm</span></span>
<span data-ttu-id="0b21b-140">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0b21b-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0b21b-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b21b-141">-WhatIf</span></span>
<span data-ttu-id="0b21b-142">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0b21b-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0b21b-143">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0b21b-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0b21b-144">-ID</span><span class="sxs-lookup"><span data-stu-id="0b21b-144">-Id</span></span>
<span data-ttu-id="0b21b-145">Die vollqualifizierte verwaltete Anwendungs-ID, einschließlich des Abonnements.</span><span class="sxs-lookup"><span data-stu-id="0b21b-145">The fully qualified managed application Id, including the subscription.</span></span> <span data-ttu-id="0b21b-146">z.b./Subscriptions/{SubscriptionId}/ResourceGroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="0b21b-146">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: System.String
Parameter Sets: The managed application Id parameter set.
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b21b-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b21b-147">CommonParameters</span></span>
<span data-ttu-id="0b21b-148">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b21b-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b21b-149">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0b21b-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b21b-150">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0b21b-150">INPUTS</span></span>

### <span data-ttu-id="0b21b-151">System. String</span><span class="sxs-lookup"><span data-stu-id="0b21b-151">System.String</span></span>
<span data-ttu-id="0b21b-152">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="0b21b-152">System.Collections.Hashtable</span></span>

## <span data-ttu-id="0b21b-153">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0b21b-153">OUTPUTS</span></span>

### <span data-ttu-id="0b21b-154">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="0b21b-154">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="0b21b-155">Notizen</span><span class="sxs-lookup"><span data-stu-id="0b21b-155">NOTES</span></span>

## <span data-ttu-id="0b21b-156">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0b21b-156">RELATED LINKS</span></span>

