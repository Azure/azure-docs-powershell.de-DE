---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: A262DFD1-8B90-462C-A4E2-ABA0F51173FA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResource.md
ms.openlocfilehash: 0cf65c33ca5af99be30f7bfa85ad4ad80ff62735
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498846"
---
# <span data-ttu-id="3753d-101">Remove-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="3753d-101">Remove-AzureRmResource</span></span>

## <span data-ttu-id="3753d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3753d-102">SYNOPSIS</span></span>
<span data-ttu-id="3753d-103">Entfernt eine Ressource.</span><span class="sxs-lookup"><span data-stu-id="3753d-103">Removes a resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3753d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3753d-104">SYNTAX</span></span>

### <span data-ttu-id="3753d-105">ByResourceId (Standard)</span><span class="sxs-lookup"><span data-stu-id="3753d-105">ByResourceId (Default)</span></span>
```
Remove-AzureRmResource [-AsJob] -ResourceId <String> [-ODataQuery <String>] [-Force] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3753d-106">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="3753d-106">BySubscriptionLevel</span></span>
```
Remove-AzureRmResource [-AsJob] -ResourceName <String> -ResourceType <String> [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ODataQuery <String>] [-ResourceGroupName <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3753d-107">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="3753d-107">ByTenantLevel</span></span>
```
Remove-AzureRmResource [-AsJob] -ResourceName <String> -ResourceType <String> [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ODataQuery <String>] [-TenantLevel] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3753d-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3753d-108">DESCRIPTION</span></span>
<span data-ttu-id="3753d-109">Das Cmdlet **Remove-AzureRmResource** entfernt eine Azure-Ressource.</span><span class="sxs-lookup"><span data-stu-id="3753d-109">The **Remove-AzureRmResource** cmdlet removes an Azure resource.</span></span>

## <span data-ttu-id="3753d-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3753d-110">EXAMPLES</span></span>

### <span data-ttu-id="3753d-111">Beispiel 1: Entfernen einer Website Ressource</span><span class="sxs-lookup"><span data-stu-id="3753d-111">Example 1: Remove a website resource</span></span>
```
PS C:\>Remove-AzureRmResource -ResourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup11/providers/Microsoft.Web/sites/ContosoSite" -Force
```

<span data-ttu-id="3753d-112">Dieser Befehl entfernt die Website Ressource mit dem Namen ContosoSite.</span><span class="sxs-lookup"><span data-stu-id="3753d-112">This command removes the website resource named ContosoSite.</span></span>
<span data-ttu-id="3753d-113">Im Beispiel wird ein Platzhalterwert für die Abonnement-ID verwendet.</span><span class="sxs-lookup"><span data-stu-id="3753d-113">The example uses a placeholder value for the subscription ID.</span></span>
<span data-ttu-id="3753d-114">Der Befehl gibt den Parameter *Force* an.</span><span class="sxs-lookup"><span data-stu-id="3753d-114">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="3753d-115">Daher werden Sie nicht zur Bestätigung aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="3753d-115">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="3753d-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="3753d-116">PARAMETERS</span></span>

### <span data-ttu-id="3753d-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="3753d-117">-ApiVersion</span></span>
<span data-ttu-id="3753d-118">Gibt die Version der zu verwendenden Ressourcenanbieter-API an.</span><span class="sxs-lookup"><span data-stu-id="3753d-118">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="3753d-119">Wenn Sie keine Version angeben, verwendet dieses Cmdlet die neueste verfügbare Version.</span><span class="sxs-lookup"><span data-stu-id="3753d-119">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="3753d-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3753d-120">-AsJob</span></span>
<span data-ttu-id="3753d-121">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="3753d-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3753d-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3753d-122">-DefaultProfile</span></span>
<span data-ttu-id="3753d-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="3753d-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3753d-124">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="3753d-124">-ExtensionResourceName</span></span>
<span data-ttu-id="3753d-125">Gibt den Namen einer Erweiterungs Ressource der Ressource an, die vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="3753d-125">Specifies the name of an extension resource of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="3753d-126">Wenn Sie beispielsweise eine Datenbank angeben möchten, verwenden Sie das folgende Format:</span><span class="sxs-lookup"><span data-stu-id="3753d-126">For instance, to specify a database, use the following format:</span></span> 

<span data-ttu-id="3753d-127">Name der Servernamen- `/` Datenbank</span><span class="sxs-lookup"><span data-stu-id="3753d-127">server name`/`database name</span></span>

```yaml
Type: String
Parameter Sets: BySubscriptionLevel, ByTenantLevel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3753d-128">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="3753d-128">-ExtensionResourceType</span></span>
<span data-ttu-id="3753d-129">Gibt den Ressourcentyp für eine Erweiterungs Ressource an.</span><span class="sxs-lookup"><span data-stu-id="3753d-129">Specifies the resource type for an extension resource.</span></span>
<span data-ttu-id="3753d-130">Gibt den Erweiterungs Ressourcentyp für die Ressource an.</span><span class="sxs-lookup"><span data-stu-id="3753d-130">Specifies the extension resource type for the resource.</span></span>
<span data-ttu-id="3753d-131">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="3753d-131">For instance:</span></span> 

`Microsoft.Sql/Servers/Databases`

```yaml
Type: String
Parameter Sets: BySubscriptionLevel, ByTenantLevel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3753d-132">-Force</span><span class="sxs-lookup"><span data-stu-id="3753d-132">-Force</span></span>
<span data-ttu-id="3753d-133">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="3753d-133">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3753d-134">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="3753d-134">-ODataQuery</span></span>
<span data-ttu-id="3753d-135">Gibt einen Open Data Protocol (OData)-stilfilter an.</span><span class="sxs-lookup"><span data-stu-id="3753d-135">Specifies an Open Data Protocol (OData) style filter.</span></span>
<span data-ttu-id="3753d-136">Dieses Cmdlet fügt zusätzlich zu anderen Filtern diesen Wert an die Anforderung an.</span><span class="sxs-lookup"><span data-stu-id="3753d-136">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="3753d-137">-Pre</span><span class="sxs-lookup"><span data-stu-id="3753d-137">-Pre</span></span>
<span data-ttu-id="3753d-138">Gibt an, dass dieses Cmdlet Pre-Release-API-Versionen berücksichtigt, wenn es automatisch die zu verwendende Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="3753d-138">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="3753d-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3753d-139">-ResourceGroupName</span></span>
<span data-ttu-id="3753d-140">Gibt den Namen der Ressourcengruppe an, aus der das Cmdlet eine Ressource entfernt.</span><span class="sxs-lookup"><span data-stu-id="3753d-140">Specifies the name of the resource group from which this cmdlet removes a resource.</span></span>

```yaml
Type: String
Parameter Sets: BySubscriptionLevel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3753d-141">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="3753d-141">-ResourceId</span></span>
<span data-ttu-id="3753d-142">Gibt die vollqualifizierte Ressourcen-ID der Ressource an, die vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="3753d-142">Specifies the fully qualified resource ID of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="3753d-143">Die ID enthält das Abonnement, wie im folgenden Beispiel:</span><span class="sxs-lookup"><span data-stu-id="3753d-143">The ID includes the subscription, as in the following example:</span></span> 

<span data-ttu-id="3753d-144">`/subscriptions/`Abonnement-ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="3753d-144">`/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3753d-145">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="3753d-145">-ResourceName</span></span>
<span data-ttu-id="3753d-146">Gibt den Namen der Ressource an, die von diesem Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="3753d-146">Specifies the name of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="3753d-147">Wenn Sie beispielsweise eine Datenbank angeben möchten, verwenden Sie das folgende Format:</span><span class="sxs-lookup"><span data-stu-id="3753d-147">For instance, to specify a database, use the following format:</span></span> 

`ContosoServer/ContosoDatabase`

```yaml
Type: String
Parameter Sets: BySubscriptionLevel, ByTenantLevel
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3753d-148">-</span><span class="sxs-lookup"><span data-stu-id="3753d-148">-ResourceType</span></span>
<span data-ttu-id="3753d-149">Gibt den Typ der Ressource an, die vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="3753d-149">Specifies the type of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="3753d-150">Bei einer Datenbank lautet der Ressourcentyp beispielsweise wie folgt:</span><span class="sxs-lookup"><span data-stu-id="3753d-150">For instance, for a database, the resource type is as follows:</span></span> 

`Microsoft.Sql/Servers/Databases`

```yaml
Type: String
Parameter Sets: BySubscriptionLevel, ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3753d-151">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="3753d-151">-TenantLevel</span></span>
<span data-ttu-id="3753d-152">Gibt an, dass dieses Cmdlet auf Mandantenebene funktioniert.</span><span class="sxs-lookup"><span data-stu-id="3753d-152">Indicates that this cmdlet operates at the tenant level.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3753d-153">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3753d-153">-Confirm</span></span>
<span data-ttu-id="3753d-154">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3753d-154">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3753d-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3753d-155">-WhatIf</span></span>
<span data-ttu-id="3753d-156">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3753d-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3753d-157">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3753d-157">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3753d-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3753d-158">CommonParameters</span></span>
<span data-ttu-id="3753d-159">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3753d-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3753d-160">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3753d-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3753d-161">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3753d-161">INPUTS</span></span>

### <span data-ttu-id="3753d-162">Keine</span><span class="sxs-lookup"><span data-stu-id="3753d-162">None</span></span>
<span data-ttu-id="3753d-163">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="3753d-163">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3753d-164">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3753d-164">OUTPUTS</span></span>

### <span data-ttu-id="3753d-165">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3753d-165">System.Boolean</span></span>

## <span data-ttu-id="3753d-166">Notizen</span><span class="sxs-lookup"><span data-stu-id="3753d-166">NOTES</span></span>

## <span data-ttu-id="3753d-167">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3753d-167">RELATED LINKS</span></span>

[<span data-ttu-id="3753d-168">Finden-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="3753d-168">Find-AzureRmResource</span></span>](./Find-AzureRmResource.md)

[<span data-ttu-id="3753d-169">Get-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="3753d-169">Get-AzureRmResource</span></span>](./Get-AzureRmResource.md)

[<span data-ttu-id="3753d-170">Verschieben-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="3753d-170">Move-AzureRmResource</span></span>](./Move-AzureRmResource.md)

[<span data-ttu-id="3753d-171">Neu – AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="3753d-171">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="3753d-172">Satz-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="3753d-172">Set-AzureRmResource</span></span>](./Set-AzureRmResource.md)


