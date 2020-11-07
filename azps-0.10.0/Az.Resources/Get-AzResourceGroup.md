---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 5B17A241-BF36-48A6-BC29-4C32C08F5F94
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-Azresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzResourceGroup.md
ms.openlocfilehash: d09031270e61be80228003ae2a9ae47a5ce5ac74
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843416"
---
# <span data-ttu-id="338c9-101">Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="338c9-101">Get-AzResourceGroup</span></span>

## <span data-ttu-id="338c9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="338c9-102">SYNOPSIS</span></span>
<span data-ttu-id="338c9-103">Ruft Ressourcengruppen ab.</span><span class="sxs-lookup"><span data-stu-id="338c9-103">Gets resource groups.</span></span>

## <span data-ttu-id="338c9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="338c9-104">SYNTAX</span></span>

### <span data-ttu-id="338c9-105">GetByResourceGroupName (Standard)</span><span class="sxs-lookup"><span data-stu-id="338c9-105">GetByResourceGroupName (Default)</span></span>
```
Get-AzResourceGroup [-Name <String>] [-Location <String>] [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="338c9-106">GetByResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="338c9-106">GetByResourceGroupId</span></span>
```
Get-AzResourceGroup [-Location <String>] [-Id <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="338c9-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="338c9-107">DESCRIPTION</span></span>
<span data-ttu-id="338c9-108">Das Cmdlet " **Get-AzResourceGroup** " ruft Azure-Ressourcengruppen im aktuellen Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="338c9-108">The **Get-AzResourceGroup** cmdlet gets Azure resource groups in the current subscription.</span></span>
<span data-ttu-id="338c9-109">Sie können alle Ressourcengruppen abrufen oder eine Ressourcengruppe nach Namen oder nach anderen Eigenschaften angeben.</span><span class="sxs-lookup"><span data-stu-id="338c9-109">You can get all resource groups, or specify a resource group by name or by other properties.</span></span>
<span data-ttu-id="338c9-110">Standardmäßig ruft dieses Cmdlet alle Ressourcengruppen im aktuellen Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="338c9-110">By default, this cmdlet gets all resource groups in the current subscription.</span></span>
<span data-ttu-id="338c9-111">Weitere Informationen zu Azure-Ressourcen und Azure-Ressourcengruppen finden Sie unter New-AzResourceGroup-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="338c9-111">For more information about Azure resources and Azure resource groups, see the New-AzResourceGroup cmdlet.</span></span>

## <span data-ttu-id="338c9-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="338c9-112">EXAMPLES</span></span>

### <span data-ttu-id="338c9-113">Beispiel 1: Abrufen einer Ressourcengruppe nach Namen</span><span class="sxs-lookup"><span data-stu-id="338c9-113">Example 1: Get a resource group by name</span></span>
```
PS C:\>Get-AzResourceGroup -Name "EngineerBlog"
```

<span data-ttu-id="338c9-114">Dieser Befehl ruft die Azure-Ressourcengruppe in Ihrem Abonnement mit dem Namen EngineerBlog ab.</span><span class="sxs-lookup"><span data-stu-id="338c9-114">This command gets the Azure resource group in your subscription named EngineerBlog.</span></span>

### <span data-ttu-id="338c9-115">Beispiel 2: Abrufen aller Kategorien einer Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="338c9-115">Example 2: Get all tags of a resource group</span></span>
```
PS C:\>(Get-AzResourceGroup -Name "ContosoRG").Tags
```

<span data-ttu-id="338c9-116">Dieser Befehl ruft die Ressourcengruppe mit dem Namen ContosoRG ab und zeigt die Tags an, die dieser Gruppe zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="338c9-116">This command gets the resource group named ContosoRG, and displays the tags associated with that group.</span></span>

### <span data-ttu-id="338c9-117">Beispiel 3: Anzeigen der Ressourcengruppen nach Standort</span><span class="sxs-lookup"><span data-stu-id="338c9-117">Example 3: Show the Resource groups by location</span></span>
```
PS C:\> Get-AzResourceGroup |
  Sort Location,ResourceGroupName |
  Format-Table -GroupBy Location ResourceGroupName,ProvisioningState,Tags
```

### <span data-ttu-id="338c9-118">Beispiel 4: Anzeigen der Namen aller Ressourcengruppen an einem bestimmten Speicherort</span><span class="sxs-lookup"><span data-stu-id="338c9-118">Example 4: Show the names of all the Resource groups in a particular location</span></span>
```
PS C:\> Get-AzResourceGroup -Location westus2 |
   Sort ResourceGroupName | 
   Format-Wide ResourceGroupName -Column 4
```

### <span data-ttu-id="338c9-119">Beispiel 5: Anzeigen der Ressourcengruppen, deren Namen mit Webserver beginnen</span><span class="sxs-lookup"><span data-stu-id="338c9-119">Example 5: Show the Resource groups whose names begin with WebServer</span></span>
```
PS C:\> Get-AzResourceGroup | Where ResourceGroupName -like WebServer*
```

## <span data-ttu-id="338c9-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="338c9-120">PARAMETERS</span></span>

### <span data-ttu-id="338c9-121">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="338c9-121">-ApiVersion</span></span>
<span data-ttu-id="338c9-122">Gibt die API-Version an, die vom Ressourcenanbieter unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="338c9-122">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="338c9-123">Sie können eine andere Version als die Standard Version angeben.</span><span class="sxs-lookup"><span data-stu-id="338c9-123">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="338c9-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="338c9-124">-DefaultProfile</span></span>
<span data-ttu-id="338c9-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="338c9-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="338c9-126">-ID</span><span class="sxs-lookup"><span data-stu-id="338c9-126">-Id</span></span>
<span data-ttu-id="338c9-127">Gibt die ID der Ressourcengruppe an, die abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="338c9-127">Specifies the ID of the resource group to get.</span></span>
<span data-ttu-id="338c9-128">Platzhalterzeichen sind nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="338c9-128">Wildcard characters are not permitted.</span></span>

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

### <span data-ttu-id="338c9-129">-Standort</span><span class="sxs-lookup"><span data-stu-id="338c9-129">-Location</span></span>
<span data-ttu-id="338c9-130">Gibt den Speicherort der Ressourcengruppe an, die abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="338c9-130">Specifies the location of the resource group to get.</span></span>

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

### <span data-ttu-id="338c9-131">-Name</span><span class="sxs-lookup"><span data-stu-id="338c9-131">-Name</span></span>
<span data-ttu-id="338c9-132">Gibt den Namen der Ressourcengruppe an, die abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="338c9-132">Specifies the name of the resource group to get.</span></span> <span data-ttu-id="338c9-133">Dieser Parameter unterstützt Platzhalter am Anfang und/oder am Ende der Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="338c9-133">This parameter supports wildcards at the beginning and/or the end of the string.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceGroupName
Aliases: ResourceGroupName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="338c9-134">-Pre</span><span class="sxs-lookup"><span data-stu-id="338c9-134">-Pre</span></span>
<span data-ttu-id="338c9-135">Gibt an, dass dieses Cmdlet Pre-Release-API-Versionen berücksichtigt, wenn es automatisch die zu verwendende Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="338c9-135">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="338c9-136">-Tag</span><span class="sxs-lookup"><span data-stu-id="338c9-136">-Tag</span></span>
<span data-ttu-id="338c9-137">Das Tag Hashtable zum Filtern von Ressourcengruppen nach.</span><span class="sxs-lookup"><span data-stu-id="338c9-137">The tag hashtable to filter resource groups by.</span></span>

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

### <span data-ttu-id="338c9-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="338c9-138">CommonParameters</span></span>
<span data-ttu-id="338c9-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="338c9-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="338c9-140">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="338c9-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="338c9-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="338c9-141">INPUTS</span></span>

### <span data-ttu-id="338c9-142">Keine</span><span class="sxs-lookup"><span data-stu-id="338c9-142">None</span></span>

## <span data-ttu-id="338c9-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="338c9-143">OUTPUTS</span></span>

### <span data-ttu-id="338c9-144">Microsoft. Azure. Commands. ResourceManagement. PSResourceGroup</span><span class="sxs-lookup"><span data-stu-id="338c9-144">Microsoft.Azure.Commands.ResourceManagement.PSResourceGroup</span></span>

## <span data-ttu-id="338c9-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="338c9-145">NOTES</span></span>

## <span data-ttu-id="338c9-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="338c9-146">RELATED LINKS</span></span>

[<span data-ttu-id="338c9-147">Neu – AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="338c9-147">New-AzResourceGroup</span></span>](./New-AzResourceGroup.md)

[<span data-ttu-id="338c9-148">Remove-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="338c9-148">Remove-AzResourceGroup</span></span>](./Remove-AzResourceGroup.md)

[<span data-ttu-id="338c9-149">Satz-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="338c9-149">Set-AzResourceGroup</span></span>](./Set-AzResourceGroup.md)


