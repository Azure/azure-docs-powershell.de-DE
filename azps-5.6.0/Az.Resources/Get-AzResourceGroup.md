---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 5B17A241-BF36-48A6-BC29-4C32C08F5F94
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroup.md
ms.openlocfilehash: e431e1e9186cdaf0ec722b5a609a3f0a9f186bd7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101929384"
---
# <span data-ttu-id="66d82-101">Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="66d82-101">Get-AzResourceGroup</span></span>

## <span data-ttu-id="66d82-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="66d82-102">SYNOPSIS</span></span>
<span data-ttu-id="66d82-103">Ruft Ressourcengruppen ab.</span><span class="sxs-lookup"><span data-stu-id="66d82-103">Gets resource groups.</span></span>

## <span data-ttu-id="66d82-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="66d82-104">SYNTAX</span></span>

### <span data-ttu-id="66d82-105">GetByResourceGroupName (Standard)</span><span class="sxs-lookup"><span data-stu-id="66d82-105">GetByResourceGroupName (Default)</span></span>
```
Get-AzResourceGroup [[-Name] <String>] [[-Location] <String>] [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="66d82-106">GetByResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="66d82-106">GetByResourceGroupId</span></span>
```
Get-AzResourceGroup [[-Location] <String>] [-Id <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="66d82-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="66d82-107">DESCRIPTION</span></span>
<span data-ttu-id="66d82-108">Das **Get-AzResourceGroup-Cmdlet** ruft Azure-Ressourcengruppen im aktuellen Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="66d82-108">The **Get-AzResourceGroup** cmdlet gets Azure resource groups in the current subscription.</span></span>
<span data-ttu-id="66d82-109">Sie können alle Ressourcengruppen erhalten oder eine Ressourcengruppe nach Namen oder anderen Eigenschaften angeben.</span><span class="sxs-lookup"><span data-stu-id="66d82-109">You can get all resource groups, or specify a resource group by name or by other properties.</span></span>
<span data-ttu-id="66d82-110">Standardmäßig ruft dieses Cmdlet alle Ressourcengruppen im aktuellen Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="66d82-110">By default, this cmdlet gets all resource groups in the current subscription.</span></span>
<span data-ttu-id="66d82-111">Weitere Informationen zu Azure-Ressourcen und Azure-Ressourcengruppen finden Sie im New-AzResourceGroup Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="66d82-111">For more information about Azure resources and Azure resource groups, see the New-AzResourceGroup cmdlet.</span></span>

## <span data-ttu-id="66d82-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="66d82-112">EXAMPLES</span></span>

### <span data-ttu-id="66d82-113">Beispiel 1: Erhalten einer Ressourcengruppe nach Name</span><span class="sxs-lookup"><span data-stu-id="66d82-113">Example 1: Get a resource group by name</span></span>
```
PS C:\> Get-AzResourceGroup -Name "EngineerBlog"
```

<span data-ttu-id="66d82-114">Dieser Befehl ruft die Azure-Ressourcengruppe in Ihrem Abonnement mit dem Namen EngineerBlog ab.</span><span class="sxs-lookup"><span data-stu-id="66d82-114">This command gets the Azure resource group in your subscription named EngineerBlog.</span></span>

### <span data-ttu-id="66d82-115">Beispiel 2: Alle Tags einer Ressourcengruppe erhalten</span><span class="sxs-lookup"><span data-stu-id="66d82-115">Example 2: Get all tags of a resource group</span></span>
```
PS C:\> (Get-AzResourceGroup -Name "ContosoRG").Tags
```

<span data-ttu-id="66d82-116">Dieser Befehl ruft die Ressourcengruppe ContosoRG ab und zeigt die tags an, die dieser Gruppe zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="66d82-116">This command gets the resource group named ContosoRG, and displays the tags associated with that group.</span></span>

### <span data-ttu-id="66d82-117">Beispiel 3: Erhalten von Ressourcengruppen basierend auf einem Tag</span><span class="sxs-lookup"><span data-stu-id="66d82-117">Example 3: Get resource groups based on tag</span></span>
```
PS C:\> Get-AzResourceGroup -Tag @{'environment'='prod'}
```

### <span data-ttu-id="66d82-118">Beispiel 4: Anzeigen der Ressourcengruppen nach Speicherort</span><span class="sxs-lookup"><span data-stu-id="66d82-118">Example 4: Show the Resource groups by location</span></span>
```
PS C:\> Get-AzResourceGroup |
  Sort Location,ResourceGroupName |
  Format-Table -GroupBy Location ResourceGroupName,ProvisioningState,Tags
```

### <span data-ttu-id="66d82-119">Beispiel 5: Anzeigen der Namen aller Ressourcengruppen an einem bestimmten Speicherort</span><span class="sxs-lookup"><span data-stu-id="66d82-119">Example 5: Show the names of all the Resource groups in a particular location</span></span>
```
PS C:\> Get-AzResourceGroup -Location westus2 |
   Sort ResourceGroupName | 
   Format-Wide ResourceGroupName -Column 4
```

### <span data-ttu-id="66d82-120">Beispiel 6: Anzeigen der Ressourcengruppen, deren Namen mit WebServer beginnen</span><span class="sxs-lookup"><span data-stu-id="66d82-120">Example 6: Show the Resource groups whose names begin with WebServer</span></span>
```
PS C:\> Get-AzResourceGroup -Name WebServer*
```

## <span data-ttu-id="66d82-121">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="66d82-121">PARAMETERS</span></span>

### <span data-ttu-id="66d82-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="66d82-122">-ApiVersion</span></span>
<span data-ttu-id="66d82-123">Gibt die vom Ressourcenanbieter unterstützte API-Version an.</span><span class="sxs-lookup"><span data-stu-id="66d82-123">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="66d82-124">Sie können eine andere Version als die Standardversion angeben.</span><span class="sxs-lookup"><span data-stu-id="66d82-124">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="66d82-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66d82-125">-DefaultProfile</span></span>
<span data-ttu-id="66d82-126">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="66d82-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="66d82-127">-ID</span><span class="sxs-lookup"><span data-stu-id="66d82-127">-Id</span></span>
<span data-ttu-id="66d82-128">Gibt die ID der zu erhaltenden Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="66d82-128">Specifies the ID of the resource group to get.</span></span>
<span data-ttu-id="66d82-129">Platzhalterzeichen sind nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="66d82-129">Wildcard characters are not permitted.</span></span>

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

### <span data-ttu-id="66d82-130">-Location</span><span class="sxs-lookup"><span data-stu-id="66d82-130">-Location</span></span>
<span data-ttu-id="66d82-131">Gibt den Speicherort der zu erhaltenden Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="66d82-131">Specifies the location of the resource group to get.</span></span>

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

### <span data-ttu-id="66d82-132">-Name</span><span class="sxs-lookup"><span data-stu-id="66d82-132">-Name</span></span>
<span data-ttu-id="66d82-133">Gibt den Namen der zu erhaltenden Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="66d82-133">Specifies the name of the resource group to get.</span></span> <span data-ttu-id="66d82-134">Dieser Parameter unterstützt Platzhalter am Anfang und/oder Ende der Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="66d82-134">This parameter supports wildcards at the beginning and/or the end of the string.</span></span>

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

### <span data-ttu-id="66d82-135">-Pre</span><span class="sxs-lookup"><span data-stu-id="66d82-135">-Pre</span></span>
<span data-ttu-id="66d82-136">Gibt an, dass dieses Cmdlet Vorabversions-API-Versionen berücksichtigt, wenn automatisch bestimmt wird, welche Version verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="66d82-136">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="66d82-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="66d82-137">-Tag</span></span>
<span data-ttu-id="66d82-138">Die #A0 zum Filtern von Ressourcengruppen nach.</span><span class="sxs-lookup"><span data-stu-id="66d82-138">The tag hashtable to filter resource groups by.</span></span>

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

### <span data-ttu-id="66d82-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66d82-139">CommonParameters</span></span>
<span data-ttu-id="66d82-140">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66d82-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66d82-141">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="66d82-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66d82-142">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="66d82-142">INPUTS</span></span>

### <span data-ttu-id="66d82-143">System.String</span><span class="sxs-lookup"><span data-stu-id="66d82-143">System.String</span></span>

### <span data-ttu-id="66d82-144">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="66d82-144">System.Collections.Hashtable</span></span>

## <span data-ttu-id="66d82-145">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="66d82-145">OUTPUTS</span></span>

### <span data-ttu-id="66d82-146">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroup</span><span class="sxs-lookup"><span data-stu-id="66d82-146">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroup</span></span>

## <span data-ttu-id="66d82-147">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="66d82-147">NOTES</span></span>

## <span data-ttu-id="66d82-148">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="66d82-148">RELATED LINKS</span></span>

[<span data-ttu-id="66d82-149">New-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="66d82-149">New-AzResourceGroup</span></span>](./New-AzResourceGroup.md)

[<span data-ttu-id="66d82-150">Remove-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="66d82-150">Remove-AzResourceGroup</span></span>](./Remove-AzResourceGroup.md)

[<span data-ttu-id="66d82-151">Set-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="66d82-151">Set-AzResourceGroup</span></span>](./Set-AzResourceGroup.md)

