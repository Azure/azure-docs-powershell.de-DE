---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: A262DFD1-8B90-462C-A4E2-ABA0F51173FA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResource.md
ms.openlocfilehash: 92d6fc81536568b2654fb72a1d6462830c05923e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500717"
---
# <span data-ttu-id="7c532-101">Remove-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="7c532-101">Remove-AzureRmResource</span></span>

## <span data-ttu-id="7c532-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7c532-102">SYNOPSIS</span></span>
<span data-ttu-id="7c532-103">Entfernt eine Ressource.</span><span class="sxs-lookup"><span data-stu-id="7c532-103">Removes a resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7c532-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7c532-104">SYNTAX</span></span>

### <span data-ttu-id="7c532-105">Die Ressourcen-ID (Standard)</span><span class="sxs-lookup"><span data-stu-id="7c532-105">The resource Id. (Default)</span></span>
```
Remove-AzureRmResource -ResourceId <String> [-ODataQuery <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7c532-106">Die Ressource, die sich auf der Abonnementebene befindet.</span><span class="sxs-lookup"><span data-stu-id="7c532-106">Resource that resides at the subscription level.</span></span>
```
Remove-AzureRmResource -ResourceName <String> -ResourceType <String> [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ODataQuery <String>] [-ResourceGroupName <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7c532-107">Die Ressource, die sich auf der Mandantenebene befindet.</span><span class="sxs-lookup"><span data-stu-id="7c532-107">Resource that resides at the tenant level.</span></span>
```
Remove-AzureRmResource -ResourceName <String> -ResourceType <String> [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ODataQuery <String>] [-TenantLevel] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7c532-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7c532-108">DESCRIPTION</span></span>
<span data-ttu-id="7c532-109">Das Cmdlet **Remove-AzureRmResource** entfernt eine Azure-Ressource.</span><span class="sxs-lookup"><span data-stu-id="7c532-109">The **Remove-AzureRmResource** cmdlet removes an Azure resource.</span></span>

## <span data-ttu-id="7c532-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7c532-110">EXAMPLES</span></span>

### <span data-ttu-id="7c532-111">Beispiel 1: Entfernen einer Website Ressource</span><span class="sxs-lookup"><span data-stu-id="7c532-111">Example 1: Remove a website resource</span></span>
```
PS C:\>Remove-AzureRmResource -ResourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup11/providers/Microsoft.Web/sites/ContosoSite" -Force
```

<span data-ttu-id="7c532-112">Dieser Befehl entfernt die Website Ressource mit dem Namen ContosoSite.</span><span class="sxs-lookup"><span data-stu-id="7c532-112">This command removes the website resource named ContosoSite.</span></span>
<span data-ttu-id="7c532-113">Im Beispiel wird ein Platzhalterwert für die Abonnement-ID verwendet.</span><span class="sxs-lookup"><span data-stu-id="7c532-113">The example uses a placeholder value for the subscription ID.</span></span>
<span data-ttu-id="7c532-114">Der Befehl gibt den Parameter *Force* an.</span><span class="sxs-lookup"><span data-stu-id="7c532-114">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="7c532-115">Daher werden Sie nicht zur Bestätigung aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="7c532-115">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="7c532-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="7c532-116">PARAMETERS</span></span>

### <span data-ttu-id="7c532-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="7c532-117">-ApiVersion</span></span>
<span data-ttu-id="7c532-118">Gibt die Version der zu verwendenden Ressourcenanbieter-API an.</span><span class="sxs-lookup"><span data-stu-id="7c532-118">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="7c532-119">Wenn Sie keine Version angeben, verwendet dieses Cmdlet die neueste verfügbare Version.</span><span class="sxs-lookup"><span data-stu-id="7c532-119">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="7c532-120">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="7c532-120">-ExtensionResourceName</span></span>
<span data-ttu-id="7c532-121">Gibt den Namen einer Erweiterungs Ressource der Ressource an, die vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="7c532-121">Specifies the name of an extension resource of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="7c532-122">Wenn Sie beispielsweise eine Datenbank angeben möchten, verwenden Sie das folgende Format:</span><span class="sxs-lookup"><span data-stu-id="7c532-122">For instance, to specify a database, use the following format:</span></span> 

<span data-ttu-id="7c532-123">Name der Servernamen- `/` Datenbank</span><span class="sxs-lookup"><span data-stu-id="7c532-123">server name`/`database name</span></span>

```yaml
Type: System.String
Parameter Sets: Resource that resides at the subscription level., Resource that resides at the tenant level.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c532-124">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="7c532-124">-ExtensionResourceType</span></span>
<span data-ttu-id="7c532-125">Gibt den Ressourcentyp für eine Erweiterungs Ressource an.</span><span class="sxs-lookup"><span data-stu-id="7c532-125">Specifies the resource type for an extension resource.</span></span>
<span data-ttu-id="7c532-126">Gibt den Erweiterungs Ressourcentyp für die Ressource an.</span><span class="sxs-lookup"><span data-stu-id="7c532-126">Specifies the extension resource type for the resource.</span></span>
<span data-ttu-id="7c532-127">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="7c532-127">For instance:</span></span> 

`Microsoft.Sql/Servers/Databases`

```yaml
Type: System.String
Parameter Sets: Resource that resides at the subscription level., Resource that resides at the tenant level.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c532-128">-Force</span><span class="sxs-lookup"><span data-stu-id="7c532-128">-Force</span></span>
<span data-ttu-id="7c532-129">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="7c532-129">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="7c532-130">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="7c532-130">-ODataQuery</span></span>
<span data-ttu-id="7c532-131">Gibt einen Open Data Protocol (OData)-stilfilter an.</span><span class="sxs-lookup"><span data-stu-id="7c532-131">Specifies an Open Data Protocol (OData) style filter.</span></span>
<span data-ttu-id="7c532-132">Dieses Cmdlet fügt zusätzlich zu anderen Filtern diesen Wert an die Anforderung an.</span><span class="sxs-lookup"><span data-stu-id="7c532-132">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="7c532-133">-Pre</span><span class="sxs-lookup"><span data-stu-id="7c532-133">-Pre</span></span>
<span data-ttu-id="7c532-134">Gibt an, dass dieses Cmdlet Pre-Release-API-Versionen berücksichtigt, wenn es automatisch die zu verwendende Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="7c532-134">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="7c532-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c532-135">-ResourceGroupName</span></span>
<span data-ttu-id="7c532-136">Gibt den Namen der Ressourcengruppe an, aus der das Cmdlet eine Ressource entfernt.</span><span class="sxs-lookup"><span data-stu-id="7c532-136">Specifies the name of the resource group from which this cmdlet removes a resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Resource that resides at the subscription level.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c532-137">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="7c532-137">-ResourceId</span></span>
<span data-ttu-id="7c532-138">Gibt die vollqualifizierte Ressourcen-ID der Ressource an, die vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="7c532-138">Specifies the fully qualified resource ID of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="7c532-139">Die ID enthält das Abonnement, wie im folgenden Beispiel:</span><span class="sxs-lookup"><span data-stu-id="7c532-139">The ID includes the subscription, as in the following example:</span></span> 

<span data-ttu-id="7c532-140">`/subscriptions/`Abonnement-ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="7c532-140">`/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

```yaml
Type: System.String
Parameter Sets: The resource Id.
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c532-141">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="7c532-141">-ResourceName</span></span>
<span data-ttu-id="7c532-142">Gibt den Namen der Ressource an, die von diesem Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="7c532-142">Specifies the name of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="7c532-143">Wenn Sie beispielsweise eine Datenbank angeben möchten, verwenden Sie das folgende Format:</span><span class="sxs-lookup"><span data-stu-id="7c532-143">For instance, to specify a database, use the following format:</span></span> 

`ContosoServer/ContosoDatabase`

```yaml
Type: System.String
Parameter Sets: Resource that resides at the subscription level., Resource that resides at the tenant level.
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c532-144">-</span><span class="sxs-lookup"><span data-stu-id="7c532-144">-ResourceType</span></span>
<span data-ttu-id="7c532-145">Gibt den Typ der Ressource an, die vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="7c532-145">Specifies the type of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="7c532-146">Bei einer Datenbank lautet der Ressourcentyp beispielsweise wie folgt:</span><span class="sxs-lookup"><span data-stu-id="7c532-146">For instance, for a database, the resource type is as follows:</span></span> 

`Microsoft.Sql/Servers/Databases`

```yaml
Type: System.String
Parameter Sets: Resource that resides at the subscription level., Resource that resides at the tenant level.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c532-147">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="7c532-147">-TenantLevel</span></span>
<span data-ttu-id="7c532-148">Gibt an, dass dieses Cmdlet auf Mandantenebene funktioniert.</span><span class="sxs-lookup"><span data-stu-id="7c532-148">Indicates that this cmdlet operates at the tenant level.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Resource that resides at the tenant level.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c532-149">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="7c532-149">-Confirm</span></span>
<span data-ttu-id="7c532-150">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7c532-150">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c532-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c532-151">-WhatIf</span></span>
<span data-ttu-id="7c532-152">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7c532-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7c532-153">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7c532-153">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c532-154">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c532-154">-DefaultProfile</span></span>
<span data-ttu-id="7c532-155">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7c532-155">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7c532-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c532-156">CommonParameters</span></span>
<span data-ttu-id="7c532-157">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c532-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c532-158">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7c532-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c532-159">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7c532-159">INPUTS</span></span>

## <span data-ttu-id="7c532-160">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7c532-160">OUTPUTS</span></span>

### <span data-ttu-id="7c532-161">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7c532-161">System.Boolean</span></span>

## <span data-ttu-id="7c532-162">Notizen</span><span class="sxs-lookup"><span data-stu-id="7c532-162">NOTES</span></span>

## <span data-ttu-id="7c532-163">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7c532-163">RELATED LINKS</span></span>

[<span data-ttu-id="7c532-164">Finden-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="7c532-164">Find-AzureRmResource</span></span>](./Find-AzureRmResource.md)

[<span data-ttu-id="7c532-165">Get-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="7c532-165">Get-AzureRmResource</span></span>](./Get-AzureRmResource.md)

[<span data-ttu-id="7c532-166">Verschieben-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="7c532-166">Move-AzureRmResource</span></span>](./Move-AzureRmResource.md)

[<span data-ttu-id="7c532-167">Neu – AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="7c532-167">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="7c532-168">Satz-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="7c532-168">Set-AzureRmResource</span></span>](./Set-AzureRmResource.md)


