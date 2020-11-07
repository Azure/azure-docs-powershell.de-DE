---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 5B17A241-BF36-48A6-BC29-4C32C08F5F94
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermresourcegroup
schema: 2.0.0
ms.openlocfilehash: ede228aef26cf7e4729acf3a6acc0faae3902f2c
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849495"
---
# <span data-ttu-id="93b14-101">Get-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="93b14-101">Get-AzureRmResourceGroup</span></span>

## <span data-ttu-id="93b14-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="93b14-102">SYNOPSIS</span></span>
<span data-ttu-id="93b14-103">Ruft Ressourcengruppen ab.</span><span class="sxs-lookup"><span data-stu-id="93b14-103">Gets resource groups.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="93b14-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="93b14-104">SYNTAX</span></span>

### <span data-ttu-id="93b14-105">GetByResourceGroupName (Standard)</span><span class="sxs-lookup"><span data-stu-id="93b14-105">GetByResourceGroupName (Default)</span></span>
```
Get-AzureRmResourceGroup [-Name <String>] [-Location <String>] [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="93b14-106">GetByResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="93b14-106">GetByResourceGroupId</span></span>
```
Get-AzureRmResourceGroup [-Location <String>] [-Id <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="93b14-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="93b14-107">DESCRIPTION</span></span>
<span data-ttu-id="93b14-108">Das Cmdlet " **Get-AzureRmResourceGroup** " ruft Azure-Ressourcengruppen im aktuellen Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="93b14-108">The **Get-AzureRmResourceGroup** cmdlet gets Azure resource groups in the current subscription.</span></span>
<span data-ttu-id="93b14-109">Sie können alle Ressourcengruppen abrufen oder eine Ressourcengruppe nach Namen oder nach anderen Eigenschaften angeben.</span><span class="sxs-lookup"><span data-stu-id="93b14-109">You can get all resource groups, or specify a resource group by name or by other properties.</span></span>
<span data-ttu-id="93b14-110">Standardmäßig ruft dieses Cmdlet alle Ressourcengruppen im aktuellen Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="93b14-110">By default, this cmdlet gets all resource groups in the current subscription.</span></span>
<span data-ttu-id="93b14-111">Weitere Informationen zu Azure-Ressourcen und Azure-Ressourcengruppen finden Sie unter New-AzureRmResourceGroup-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="93b14-111">For more information about Azure resources and Azure resource groups, see the New-AzureRmResourceGroup cmdlet.</span></span>

## <span data-ttu-id="93b14-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="93b14-112">EXAMPLES</span></span>

### <span data-ttu-id="93b14-113">Beispiel 1: Abrufen einer Ressourcengruppe nach Namen</span><span class="sxs-lookup"><span data-stu-id="93b14-113">Example 1: Get a resource group by name</span></span>
```
PS C:\>Get-AzureRmResourceGroup -Name "EngineerBlog"
```

<span data-ttu-id="93b14-114">Dieser Befehl ruft die Azure-Ressourcengruppe in Ihrem Abonnement mit dem Namen EngineerBlog ab.</span><span class="sxs-lookup"><span data-stu-id="93b14-114">This command gets the Azure resource group in your subscription named EngineerBlog.</span></span>

### <span data-ttu-id="93b14-115">Beispiel 2: Abrufen aller Kategorien einer Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="93b14-115">Example 2: Get all tags of a resource group</span></span>
```
PS C:\>(Get-AzureRmResourceGroup -Name "ContosoRG").Tags
```

<span data-ttu-id="93b14-116">Dieser Befehl ruft die Ressourcengruppe mit dem Namen ContosoRG ab und zeigt die Tags an, die dieser Gruppe zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="93b14-116">This command gets the resource group named ContosoRG, and displays the tags associated with that group.</span></span>

### <span data-ttu-id="93b14-117">Beispiel 3: Anzeigen der Ressourcengruppen nach Standort</span><span class="sxs-lookup"><span data-stu-id="93b14-117">Example 3: Show the Resource groups by location</span></span>
```
PS C:\> Get-AzureRmResourceGroup |
  Sort Location,ResourceGroupName |
  Format-Table -GroupBy Location ResourceGroupName,ProvisioningState,Tags
```

### <span data-ttu-id="93b14-118">Beispiel 4: Anzeigen der Namen aller Ressourcengruppen an einem bestimmten Speicherort</span><span class="sxs-lookup"><span data-stu-id="93b14-118">Example 4: Show the names of all the Resource groups in a particular location</span></span>
```
PS C:\> Get-AzureRmResourceGroup -Location westus2 |
   Sort ResourceGroupName | 
   Format-Wide ResourceGroupName -Column 4
```

### <span data-ttu-id="93b14-119">Beispiel 5: Anzeigen der Ressourcengruppen, deren Namen mit Webserver beginnen</span><span class="sxs-lookup"><span data-stu-id="93b14-119">Example 5: Show the Resource groups whose names begin with WebServer</span></span>
```
PS C:\> Get-AzureRmResourceGroup | Where ResourceGroupName -like WebServer*
```

## <span data-ttu-id="93b14-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="93b14-120">PARAMETERS</span></span>

### <span data-ttu-id="93b14-121">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="93b14-121">-ApiVersion</span></span>
<span data-ttu-id="93b14-122">Gibt die API-Version an, die vom Ressourcenanbieter unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="93b14-122">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="93b14-123">Sie können eine andere Version als die Standard Version angeben.</span><span class="sxs-lookup"><span data-stu-id="93b14-123">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="93b14-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93b14-124">-DefaultProfile</span></span>
<span data-ttu-id="93b14-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="93b14-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="93b14-126">-ID</span><span class="sxs-lookup"><span data-stu-id="93b14-126">-Id</span></span>
<span data-ttu-id="93b14-127">Gibt die ID der Ressourcengruppe an, die abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="93b14-127">Specifies the ID of the resource group to get.</span></span>
<span data-ttu-id="93b14-128">Platzhalterzeichen sind nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="93b14-128">Wildcard characters are not permitted.</span></span>

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

### <span data-ttu-id="93b14-129">-Standort</span><span class="sxs-lookup"><span data-stu-id="93b14-129">-Location</span></span>
<span data-ttu-id="93b14-130">Gibt den Speicherort der Ressourcengruppe an, die abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="93b14-130">Specifies the location of the resource group to get.</span></span>

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

### <span data-ttu-id="93b14-131">-Name</span><span class="sxs-lookup"><span data-stu-id="93b14-131">-Name</span></span>
<span data-ttu-id="93b14-132">Gibt den Namen der Ressourcengruppe an, die abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="93b14-132">Specifies the name of the resource group to get.</span></span> <span data-ttu-id="93b14-133">Dieser Parameter unterstützt Platzhalter am Anfang und/oder am Ende der Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="93b14-133">This parameter supports wildcards at the beginning and/or the end of the string.</span></span>

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

### <span data-ttu-id="93b14-134">-Pre</span><span class="sxs-lookup"><span data-stu-id="93b14-134">-Pre</span></span>
<span data-ttu-id="93b14-135">Gibt an, dass dieses Cmdlet Pre-Release-API-Versionen berücksichtigt, wenn es automatisch die zu verwendende Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="93b14-135">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="93b14-136">-Tag</span><span class="sxs-lookup"><span data-stu-id="93b14-136">-Tag</span></span>
<span data-ttu-id="93b14-137">Das Tag Hashtable zum Filtern von Ressourcengruppen nach.</span><span class="sxs-lookup"><span data-stu-id="93b14-137">The tag hashtable to filter resource groups by.</span></span>

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

### <span data-ttu-id="93b14-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93b14-138">CommonParameters</span></span>
<span data-ttu-id="93b14-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93b14-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93b14-140">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="93b14-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93b14-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="93b14-141">INPUTS</span></span>

### <span data-ttu-id="93b14-142">Keine</span><span class="sxs-lookup"><span data-stu-id="93b14-142">None</span></span>

## <span data-ttu-id="93b14-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="93b14-143">OUTPUTS</span></span>

### <span data-ttu-id="93b14-144">Microsoft. Azure. Commands. ResourceManagement. PSResourceGroup</span><span class="sxs-lookup"><span data-stu-id="93b14-144">Microsoft.Azure.Commands.ResourceManagement.PSResourceGroup</span></span>

## <span data-ttu-id="93b14-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="93b14-145">NOTES</span></span>

## <span data-ttu-id="93b14-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="93b14-146">RELATED LINKS</span></span>

[<span data-ttu-id="93b14-147">Neu – AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="93b14-147">New-AzureRmResourceGroup</span></span>](./New-AzureRmResourceGroup.md)

[<span data-ttu-id="93b14-148">Remove-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="93b14-148">Remove-AzureRmResourceGroup</span></span>](./Remove-AzureRmResourceGroup.md)

[<span data-ttu-id="93b14-149">Satz-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="93b14-149">Set-AzureRmResourceGroup</span></span>](./Set-AzureRmResourceGroup.md)


