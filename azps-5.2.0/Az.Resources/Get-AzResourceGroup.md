---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 5B17A241-BF36-48A6-BC29-4C32C08F5F94
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroup.md
ms.openlocfilehash: 9c7c002861832da3e871b49f03753608ba48268d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98298168"
---
# <span data-ttu-id="22207-101">Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="22207-101">Get-AzResourceGroup</span></span>

## <span data-ttu-id="22207-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="22207-102">SYNOPSIS</span></span>
<span data-ttu-id="22207-103">Ruft Ressourcengruppen ab.</span><span class="sxs-lookup"><span data-stu-id="22207-103">Gets resource groups.</span></span>

## <span data-ttu-id="22207-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="22207-104">SYNTAX</span></span>

### <span data-ttu-id="22207-105">GetByResourceGroupName (Standard)</span><span class="sxs-lookup"><span data-stu-id="22207-105">GetByResourceGroupName (Default)</span></span>
```
Get-AzResourceGroup [[-Name] <String>] [[-Location] <String>] [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="22207-106">GetByResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="22207-106">GetByResourceGroupId</span></span>
```
Get-AzResourceGroup [[-Location] <String>] [-Id <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="22207-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="22207-107">DESCRIPTION</span></span>
<span data-ttu-id="22207-108">Das **Cmdlet "Get-AzResourceGroup"** ruft Die Azure-Ressourcengruppen im aktuellen Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="22207-108">The **Get-AzResourceGroup** cmdlet gets Azure resource groups in the current subscription.</span></span>
<span data-ttu-id="22207-109">Sie können alle Ressourcengruppen erhalten oder eine Ressourcengruppe nach Name oder anderen Eigenschaften angeben.</span><span class="sxs-lookup"><span data-stu-id="22207-109">You can get all resource groups, or specify a resource group by name or by other properties.</span></span>
<span data-ttu-id="22207-110">Standardmäßig ruft dieses Cmdlet alle Ressourcengruppen im aktuellen Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="22207-110">By default, this cmdlet gets all resource groups in the current subscription.</span></span>
<span data-ttu-id="22207-111">Weitere Informationen zu Azure-Ressourcen und -Ressourcengruppen finden Sie im New-AzResourceGroup-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="22207-111">For more information about Azure resources and Azure resource groups, see the New-AzResourceGroup cmdlet.</span></span>

## <span data-ttu-id="22207-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="22207-112">EXAMPLES</span></span>

### <span data-ttu-id="22207-113">Beispiel 1: Erhalten einer Ressourcengruppe nach Name</span><span class="sxs-lookup"><span data-stu-id="22207-113">Example 1: Get a resource group by name</span></span>
```
PS C:\> Get-AzResourceGroup -Name "EngineerBlog"
```

<span data-ttu-id="22207-114">Dieser Befehl ruft die Azure-Ressourcengruppe in Ihrem Abonnement namens "EngineerBlog" ab.</span><span class="sxs-lookup"><span data-stu-id="22207-114">This command gets the Azure resource group in your subscription named EngineerBlog.</span></span>

### <span data-ttu-id="22207-115">Beispiel 2: Alle Tags einer Ressourcengruppe erhalten</span><span class="sxs-lookup"><span data-stu-id="22207-115">Example 2: Get all tags of a resource group</span></span>
```
PS C:\> (Get-AzResourceGroup -Name "ContosoRG").Tags
```

<span data-ttu-id="22207-116">Dieser Befehl ruft die Ressourcengruppe "ContosoRG" ab und zeigt die dieser Gruppe zugeordneten Tags an.</span><span class="sxs-lookup"><span data-stu-id="22207-116">This command gets the resource group named ContosoRG, and displays the tags associated with that group.</span></span>

### <span data-ttu-id="22207-117">Beispiel 3: Ressourcengruppen auf Der Grundlage eines Tags erhalten</span><span class="sxs-lookup"><span data-stu-id="22207-117">Example 3: Get resource groups based on tag</span></span>
```
PS C:\> Get-AzResourceGroup -Tag @{'environment'='prod'}
```

### <span data-ttu-id="22207-118">Beispiel 4: Anzeigen der Ressourcengruppen nach Ort</span><span class="sxs-lookup"><span data-stu-id="22207-118">Example 4: Show the Resource groups by location</span></span>
```
PS C:\> Get-AzResourceGroup |
  Sort Location,ResourceGroupName |
  Format-Table -GroupBy Location ResourceGroupName,ProvisioningState,Tags
```

### <span data-ttu-id="22207-119">Beispiel 5: Anzeigen der Namen aller Ressourcengruppen an einem bestimmten Ort</span><span class="sxs-lookup"><span data-stu-id="22207-119">Example 5: Show the names of all the Resource groups in a particular location</span></span>
```
PS C:\> Get-AzResourceGroup -Location westus2 |
   Sort ResourceGroupName | 
   Format-Wide ResourceGroupName -Column 4
```

### <span data-ttu-id="22207-120">Beispiel 6: Anzeigen der Ressourcengruppen, deren Namen mit WebServer beginnen</span><span class="sxs-lookup"><span data-stu-id="22207-120">Example 6: Show the Resource groups whose names begin with WebServer</span></span>
```
PS C:\> Get-AzResourceGroup -Name WebServer*
```

## <span data-ttu-id="22207-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="22207-121">PARAMETERS</span></span>

### <span data-ttu-id="22207-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="22207-122">-ApiVersion</span></span>
<span data-ttu-id="22207-123">Gibt die vom Ressourcenanbieter unterstützte API-Version an.</span><span class="sxs-lookup"><span data-stu-id="22207-123">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="22207-124">Sie können eine andere Version als die Standardversion angeben.</span><span class="sxs-lookup"><span data-stu-id="22207-124">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="22207-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22207-125">-DefaultProfile</span></span>
<span data-ttu-id="22207-126">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="22207-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="22207-127">-ID</span><span class="sxs-lookup"><span data-stu-id="22207-127">-Id</span></span>
<span data-ttu-id="22207-128">Gibt die ID der ressourcengruppe an, die sie erhalten soll.</span><span class="sxs-lookup"><span data-stu-id="22207-128">Specifies the ID of the resource group to get.</span></span>
<span data-ttu-id="22207-129">Platzhalterzeichen sind nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="22207-129">Wildcard characters are not permitted.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceGroupId
Aliases: ResourceGroupId, ResourceId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22207-130">-Location</span><span class="sxs-lookup"><span data-stu-id="22207-130">-Location</span></span>
<span data-ttu-id="22207-131">Gibt den Speicherort der Ressourcengruppe an, die sie erhalten soll.</span><span class="sxs-lookup"><span data-stu-id="22207-131">Specifies the location of the resource group to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22207-132">-Name</span><span class="sxs-lookup"><span data-stu-id="22207-132">-Name</span></span>
<span data-ttu-id="22207-133">Gibt den Namen der Ressourcengruppe an, die sie erhalten soll.</span><span class="sxs-lookup"><span data-stu-id="22207-133">Specifies the name of the resource group to get.</span></span> <span data-ttu-id="22207-134">Dieser Parameter unterstützt Platzhalter am Anfang und/oder Ende der Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="22207-134">This parameter supports wildcards at the beginning and/or the end of the string.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceGroupName
Aliases: ResourceGroupName

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="22207-135">-Pre</span><span class="sxs-lookup"><span data-stu-id="22207-135">-Pre</span></span>
<span data-ttu-id="22207-136">Gibt an, dass dieses Cmdlet Vorabversions-API-Versionen berücksichtigt, wenn automatisch bestimmt wird, welche Version verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="22207-136">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="22207-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="22207-137">-Tag</span></span>
<span data-ttu-id="22207-138">Die Hashtabelle für das Tag zum Filtern von Ressourcengruppen.</span><span class="sxs-lookup"><span data-stu-id="22207-138">The tag hashtable to filter resource groups by.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: GetByResourceGroupName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22207-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22207-139">CommonParameters</span></span>
<span data-ttu-id="22207-140">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22207-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22207-141">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="22207-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22207-142">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="22207-142">INPUTS</span></span>

### <span data-ttu-id="22207-143">System.String</span><span class="sxs-lookup"><span data-stu-id="22207-143">System.String</span></span>

### <span data-ttu-id="22207-144">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="22207-144">System.Collections.Hashtable</span></span>

## <span data-ttu-id="22207-145">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="22207-145">OUTPUTS</span></span>

### <span data-ttu-id="22207-146">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroup</span><span class="sxs-lookup"><span data-stu-id="22207-146">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroup</span></span>

## <span data-ttu-id="22207-147">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="22207-147">NOTES</span></span>

## <span data-ttu-id="22207-148">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="22207-148">RELATED LINKS</span></span>

[<span data-ttu-id="22207-149">New-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="22207-149">New-AzResourceGroup</span></span>](./New-AzResourceGroup.md)

[<span data-ttu-id="22207-150">Remove-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="22207-150">Remove-AzResourceGroup</span></span>](./Remove-AzResourceGroup.md)

[<span data-ttu-id="22207-151">Set-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="22207-151">Set-AzResourceGroup</span></span>](./Set-AzResourceGroup.md)

