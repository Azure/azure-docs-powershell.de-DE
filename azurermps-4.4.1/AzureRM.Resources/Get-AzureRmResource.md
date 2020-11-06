---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: C2C608E5-3351-4D01-8533-9668B2E9F1D1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResource.md
ms.openlocfilehash: 01e4e6b990a35b8573a9ea1d2f2803f6d6fabc1a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500770"
---
# <span data-ttu-id="e7254-101">Get-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="e7254-101">Get-AzureRmResource</span></span>

## <span data-ttu-id="e7254-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e7254-102">SYNOPSIS</span></span>
<span data-ttu-id="e7254-103">Ruft Ressourcen ab.</span><span class="sxs-lookup"><span data-stu-id="e7254-103">Gets resources.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e7254-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e7254-104">SYNTAX</span></span>

### <span data-ttu-id="e7254-105">Der Parametersatz "alle Ressourcen auflisten"</span><span class="sxs-lookup"><span data-stu-id="e7254-105">The list all resources parameter set.</span></span> <span data-ttu-id="e7254-106">Standard</span><span class="sxs-lookup"><span data-stu-id="e7254-106">(Default)</span></span>
```
Get-AzureRmResource [-ExpandProperties] [-ODataQuery <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e7254-107">Abrufen einer einzelnen Ressource anhand der ID</span><span class="sxs-lookup"><span data-stu-id="e7254-107">Get a single resource by its Id.</span></span>
```
Get-AzureRmResource -ResourceId <String> [-ExpandProperties] [-ODataQuery <String>] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e7254-108">Abrufen einer einzelnen Ressource auf Mandantenebene</span><span class="sxs-lookup"><span data-stu-id="e7254-108">Get a single resource at the tenant level.</span></span>
```
Get-AzureRmResource -ResourceName <String> -ResourceType <String> [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ExpandProperties] [-IsCollection] [-ODataQuery <String>] [-TenantLevel]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e7254-109">Listet die Ressourcen auf der Grundlage des angegebenen Bereichs auf Mandantenebene auf.</span><span class="sxs-lookup"><span data-stu-id="e7254-109">Lists the resources based on the specified scope at the tenant level.</span></span>
```
Get-AzureRmResource [-ResourceName <String>] [-ResourceType <String>] [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ExpandProperties] [-IsCollection] [-Top <Int32>] [-ODataQuery <String>]
 [-TenantLevel] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e7254-110">Abrufen einer Ressource nach Name und Gruppe</span><span class="sxs-lookup"><span data-stu-id="e7254-110">Get resource by name and group</span></span>
```
Get-AzureRmResource [-ResourceName <String>] [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ExpandProperties] [-IsCollection] [-ODataQuery <String>]
 [-ResourceGroupName <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e7254-111">Abrufen einer Ressource nach Name und Typ</span><span class="sxs-lookup"><span data-stu-id="e7254-111">Get a resource by name and type.</span></span>
```
Get-AzureRmResource [-ResourceName <String>] [-ResourceType <String>] [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ExpandProperties] [-IsCollection] [-ODataQuery <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e7254-112">Abrufen einer Ressource nach Name, Gruppe und Typ</span><span class="sxs-lookup"><span data-stu-id="e7254-112">Get resource by name, group and type</span></span>
```
Get-AzureRmResource -ResourceName <String> -ResourceType <String> [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ExpandProperties] [-ODataQuery <String>] -ResourceGroupName <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e7254-113">Abrufen der Ressourcensammlung</span><span class="sxs-lookup"><span data-stu-id="e7254-113">Get resource collection</span></span>
```
Get-AzureRmResource [-ResourceType <String>] [-ExtensionResourceType <String>] [-ExpandProperties]
 [-IsCollection] [-ODataQuery <String>] [-ResourceGroupName <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e7254-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e7254-114">DESCRIPTION</span></span>
<span data-ttu-id="e7254-115">Das Cmdlet " **Get-AzureRmResource** " ruft Azure-Ressourcen ab.</span><span class="sxs-lookup"><span data-stu-id="e7254-115">The **Get-AzureRmResource** cmdlet gets Azure resources.</span></span>

## <span data-ttu-id="e7254-116">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e7254-116">EXAMPLES</span></span>

### <span data-ttu-id="e7254-117">Beispiel 1: Abrufen einer Ressource</span><span class="sxs-lookup"><span data-stu-id="e7254-117">Example 1: Get a resource</span></span>
```
PS C:\>Get-AzureRmResource -ResourceType "microsoft.web/sites" -ResourceGroupName "ResourceGroup11" -ResourceName "ContosoWebsite"
```

<span data-ttu-id="e7254-118">Dieser Befehl ruft eine Ressource des Typs Microsoft. Web/Websites mit dem Namen ContosoWebsite unter ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="e7254-118">This command gets a resource of the type microsoft.web/sites, named ContosoWebsite under ResourceGroup11.</span></span>

## <span data-ttu-id="e7254-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="e7254-119">PARAMETERS</span></span>

### <span data-ttu-id="e7254-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="e7254-120">-ApiVersion</span></span>
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

### <span data-ttu-id="e7254-121">-ExpandProperties</span><span class="sxs-lookup"><span data-stu-id="e7254-121">-ExpandProperties</span></span>
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

### <span data-ttu-id="e7254-122">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="e7254-122">-ExtensionResourceName</span></span>
```yaml
Type: System.String
Parameter Sets: Get a single resource at the tenant level., Lists the resources based on the specified scope at the tenant level., Get resource by name and group, Get a resource by name and type., Get resource by name, group and type
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7254-123">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="e7254-123">-ExtensionResourceType</span></span>
```yaml
Type: System.String
Parameter Sets: Get a single resource at the tenant level., Lists the resources based on the specified scope at the tenant level., Get resource by name and group, Get a resource by name and type., Get resource by name, group and type
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Get resource collection
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7254-124">-IsCollection</span><span class="sxs-lookup"><span data-stu-id="e7254-124">-IsCollection</span></span>
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Get a single resource at the tenant level., Lists the resources based on the specified scope at the tenant level., Get resource by name and group, Get a resource by name and type., Get resource collection
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7254-125">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="e7254-125">-ODataQuery</span></span>
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

### <span data-ttu-id="e7254-126">-Pre</span><span class="sxs-lookup"><span data-stu-id="e7254-126">-Pre</span></span>
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

### <span data-ttu-id="e7254-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7254-127">-ResourceGroupName</span></span>
```yaml
Type: System.String
Parameter Sets: Get resource by name and group
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Get resource by name, group and type
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Get resource collection
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7254-128">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="e7254-128">-ResourceId</span></span>
<span data-ttu-id="e7254-129">Gibt die vollqualifizierte Ressourcen-ID an, einschließlich des Abonnements, wie im folgenden Beispiel:</span><span class="sxs-lookup"><span data-stu-id="e7254-129">Specifies the fully qualified resource ID, including the subscription, as in the following example:</span></span> 

<span data-ttu-id="e7254-130">`/subscriptions/`Abonnement-ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="e7254-130">`/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

<span data-ttu-id="e7254-131">Dieses Cmdlet ruft die Ressource ab, die diese ID hat.</span><span class="sxs-lookup"><span data-stu-id="e7254-131">This cmdlet gets the resource that has this ID.</span></span>

```yaml
Type: System.String
Parameter Sets: Get a single resource by its Id.
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7254-132">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="e7254-132">-ResourceName</span></span>
```yaml
Type: System.String
Parameter Sets: Get a single resource at the tenant level., Get resource by name, group and type
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Lists the resources based on the specified scope at the tenant level., Get resource by name and group, Get a resource by name and type.
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7254-133">-</span><span class="sxs-lookup"><span data-stu-id="e7254-133">-ResourceType</span></span>
```yaml
Type: System.String
Parameter Sets: Get a single resource at the tenant level., Get resource by name, group and type
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Lists the resources based on the specified scope at the tenant level., Get a resource by name and type.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Get resource collection
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7254-134">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="e7254-134">-TenantLevel</span></span>
<span data-ttu-id="e7254-135">Gibt an, dass dieses Cmdlet auf Mandantenebene funktioniert.</span><span class="sxs-lookup"><span data-stu-id="e7254-135">Indicates that this cmdlet operates at the tenant level.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Get a single resource at the tenant level., Lists the resources based on the specified scope at the tenant level.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7254-136">-Top</span><span class="sxs-lookup"><span data-stu-id="e7254-136">-Top</span></span>
```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: Lists the resources based on the specified scope at the tenant level.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7254-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7254-137">-DefaultProfile</span></span>
<span data-ttu-id="e7254-138">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e7254-138">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e7254-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7254-139">CommonParameters</span></span>
<span data-ttu-id="e7254-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7254-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7254-141">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e7254-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7254-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e7254-142">INPUTS</span></span>

## <span data-ttu-id="e7254-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e7254-143">OUTPUTS</span></span>

### <span data-ttu-id="e7254-144">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="e7254-144">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="e7254-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="e7254-145">NOTES</span></span>

## <span data-ttu-id="e7254-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e7254-146">RELATED LINKS</span></span>

[<span data-ttu-id="e7254-147">Finden-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="e7254-147">Find-AzureRmResource</span></span>](./Find-AzureRmResource.md)

[<span data-ttu-id="e7254-148">Verschieben-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="e7254-148">Move-AzureRmResource</span></span>](./Move-AzureRmResource.md)

[<span data-ttu-id="e7254-149">Neu – AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="e7254-149">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="e7254-150">Remove-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="e7254-150">Remove-AzureRmResource</span></span>](./Remove-AzureRmResource.md)

[<span data-ttu-id="e7254-151">Satz-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="e7254-151">Set-AzureRmResource</span></span>](./Set-AzureRmResource.md)


