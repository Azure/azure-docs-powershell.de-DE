---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 5B17A241-BF36-48A6-BC29-4C32C08F5F94
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroup.md
ms.openlocfilehash: b8e74a0c349ea058d05ef044648e836fddc1f7b3
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94166648"
---
# <span data-ttu-id="b19b1-101">Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="b19b1-101">Get-AzResourceGroup</span></span>

## <span data-ttu-id="b19b1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b19b1-102">SYNOPSIS</span></span>
<span data-ttu-id="b19b1-103">Ruft Ressourcengruppen ab.</span><span class="sxs-lookup"><span data-stu-id="b19b1-103">Gets resource groups.</span></span>

## <span data-ttu-id="b19b1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b19b1-104">SYNTAX</span></span>

### <span data-ttu-id="b19b1-105">GetByResourceGroupName (Standard)</span><span class="sxs-lookup"><span data-stu-id="b19b1-105">GetByResourceGroupName (Default)</span></span>
```
Get-AzResourceGroup [[-Name] <String>] [[-Location] <String>] [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b19b1-106">GetByResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="b19b1-106">GetByResourceGroupId</span></span>
```
Get-AzResourceGroup [[-Location] <String>] [-Id <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b19b1-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b19b1-107">DESCRIPTION</span></span>
<span data-ttu-id="b19b1-108">Das Cmdlet " **Get-AzResourceGroup** " ruft Azure-Ressourcengruppen im aktuellen Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="b19b1-108">The **Get-AzResourceGroup** cmdlet gets Azure resource groups in the current subscription.</span></span>
<span data-ttu-id="b19b1-109">Sie können alle Ressourcengruppen abrufen oder eine Ressourcengruppe nach Namen oder nach anderen Eigenschaften angeben.</span><span class="sxs-lookup"><span data-stu-id="b19b1-109">You can get all resource groups, or specify a resource group by name or by other properties.</span></span>
<span data-ttu-id="b19b1-110">Standardmäßig ruft dieses Cmdlet alle Ressourcengruppen im aktuellen Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="b19b1-110">By default, this cmdlet gets all resource groups in the current subscription.</span></span>
<span data-ttu-id="b19b1-111">Weitere Informationen zu Azure-Ressourcen und Azure-Ressourcengruppen finden Sie unter New-AzResourceGroup-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b19b1-111">For more information about Azure resources and Azure resource groups, see the New-AzResourceGroup cmdlet.</span></span>

## <span data-ttu-id="b19b1-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b19b1-112">EXAMPLES</span></span>

### <span data-ttu-id="b19b1-113">Beispiel 1: Abrufen einer Ressourcengruppe nach Namen</span><span class="sxs-lookup"><span data-stu-id="b19b1-113">Example 1: Get a resource group by name</span></span>
```
PS C:\> Get-AzResourceGroup -Name "EngineerBlog"
```

<span data-ttu-id="b19b1-114">Dieser Befehl ruft die Azure-Ressourcengruppe in Ihrem Abonnement mit dem Namen EngineerBlog ab.</span><span class="sxs-lookup"><span data-stu-id="b19b1-114">This command gets the Azure resource group in your subscription named EngineerBlog.</span></span>

### <span data-ttu-id="b19b1-115">Beispiel 2: Abrufen aller Kategorien einer Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="b19b1-115">Example 2: Get all tags of a resource group</span></span>
```
PS C:\> (Get-AzResourceGroup -Name "ContosoRG").Tags
```

<span data-ttu-id="b19b1-116">Dieser Befehl ruft die Ressourcengruppe mit dem Namen ContosoRG ab und zeigt die Tags an, die dieser Gruppe zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="b19b1-116">This command gets the resource group named ContosoRG, and displays the tags associated with that group.</span></span>

### <span data-ttu-id="b19b1-117">Beispiel 3: Abrufen von Ressourcengruppen basierend auf dem Tag</span><span class="sxs-lookup"><span data-stu-id="b19b1-117">Example 3: Get resource groups based on tag</span></span>
```
PS C:\> Get-AzResourceGroup -Tag @{'environment'='prod'}
```

### <span data-ttu-id="b19b1-118">Beispiel 4: Anzeigen der Ressourcengruppen nach Standort</span><span class="sxs-lookup"><span data-stu-id="b19b1-118">Example 4: Show the Resource groups by location</span></span>
```
PS C:\> Get-AzResourceGroup |
  Sort Location,ResourceGroupName |
  Format-Table -GroupBy Location ResourceGroupName,ProvisioningState,Tags
```

### <span data-ttu-id="b19b1-119">Beispiel 5: Anzeigen der Namen aller Ressourcengruppen an einem bestimmten Speicherort</span><span class="sxs-lookup"><span data-stu-id="b19b1-119">Example 5: Show the names of all the Resource groups in a particular location</span></span>
```
PS C:\> Get-AzResourceGroup -Location westus2 |
   Sort ResourceGroupName | 
   Format-Wide ResourceGroupName -Column 4
```

### <span data-ttu-id="b19b1-120">Beispiel 6: Anzeigen der Ressourcengruppen, deren Namen mit Webserver beginnen</span><span class="sxs-lookup"><span data-stu-id="b19b1-120">Example 6: Show the Resource groups whose names begin with WebServer</span></span>
```
PS C:\> Get-AzResourceGroup -Name WebServer*
```

## <span data-ttu-id="b19b1-121">Parameter</span><span class="sxs-lookup"><span data-stu-id="b19b1-121">PARAMETERS</span></span>

### <span data-ttu-id="b19b1-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="b19b1-122">-ApiVersion</span></span>
<span data-ttu-id="b19b1-123">Gibt die API-Version an, die vom Ressourcenanbieter unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="b19b1-123">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="b19b1-124">Sie können eine andere Version als die Standard Version angeben.</span><span class="sxs-lookup"><span data-stu-id="b19b1-124">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="b19b1-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b19b1-125">-DefaultProfile</span></span>
<span data-ttu-id="b19b1-126">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="b19b1-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b19b1-127">-ID</span><span class="sxs-lookup"><span data-stu-id="b19b1-127">-Id</span></span>
<span data-ttu-id="b19b1-128">Gibt die ID der Ressourcengruppe an, die abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="b19b1-128">Specifies the ID of the resource group to get.</span></span>
<span data-ttu-id="b19b1-129">Platzhalterzeichen sind nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="b19b1-129">Wildcard characters are not permitted.</span></span>

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

### <span data-ttu-id="b19b1-130">-Standort</span><span class="sxs-lookup"><span data-stu-id="b19b1-130">-Location</span></span>
<span data-ttu-id="b19b1-131">Gibt den Speicherort der Ressourcengruppe an, die abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="b19b1-131">Specifies the location of the resource group to get.</span></span>

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

### <span data-ttu-id="b19b1-132">-Name</span><span class="sxs-lookup"><span data-stu-id="b19b1-132">-Name</span></span>
<span data-ttu-id="b19b1-133">Gibt den Namen der Ressourcengruppe an, die abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="b19b1-133">Specifies the name of the resource group to get.</span></span> <span data-ttu-id="b19b1-134">Dieser Parameter unterstützt Platzhalter am Anfang und/oder am Ende der Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="b19b1-134">This parameter supports wildcards at the beginning and/or the end of the string.</span></span>

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

### <span data-ttu-id="b19b1-135">-Pre</span><span class="sxs-lookup"><span data-stu-id="b19b1-135">-Pre</span></span>
<span data-ttu-id="b19b1-136">Gibt an, dass dieses Cmdlet Pre-Release-API-Versionen berücksichtigt, wenn es automatisch die zu verwendende Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="b19b1-136">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="b19b1-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="b19b1-137">-Tag</span></span>
<span data-ttu-id="b19b1-138">Das Tag Hashtable zum Filtern von Ressourcengruppen nach.</span><span class="sxs-lookup"><span data-stu-id="b19b1-138">The tag hashtable to filter resource groups by.</span></span>

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

### <span data-ttu-id="b19b1-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b19b1-139">CommonParameters</span></span>
<span data-ttu-id="b19b1-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b19b1-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b19b1-141">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b19b1-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b19b1-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b19b1-142">INPUTS</span></span>

### <span data-ttu-id="b19b1-143">System. String</span><span class="sxs-lookup"><span data-stu-id="b19b1-143">System.String</span></span>

### <span data-ttu-id="b19b1-144">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="b19b1-144">System.Collections.Hashtable</span></span>

## <span data-ttu-id="b19b1-145">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b19b1-145">OUTPUTS</span></span>

### <span data-ttu-id="b19b1-146">Microsoft. Azure. Commands. ResourceManager. Cmdlets. SdkModels. PSResourceGroup</span><span class="sxs-lookup"><span data-stu-id="b19b1-146">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroup</span></span>

## <span data-ttu-id="b19b1-147">Notizen</span><span class="sxs-lookup"><span data-stu-id="b19b1-147">NOTES</span></span>

## <span data-ttu-id="b19b1-148">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b19b1-148">RELATED LINKS</span></span>

[<span data-ttu-id="b19b1-149">Neu – AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="b19b1-149">New-AzResourceGroup</span></span>](./New-AzResourceGroup.md)

[<span data-ttu-id="b19b1-150">Remove-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="b19b1-150">Remove-AzResourceGroup</span></span>](./Remove-AzResourceGroup.md)

[<span data-ttu-id="b19b1-151">Satz-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="b19b1-151">Set-AzResourceGroup</span></span>](./Set-AzResourceGroup.md)


