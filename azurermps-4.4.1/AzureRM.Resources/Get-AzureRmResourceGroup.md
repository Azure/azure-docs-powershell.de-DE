---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 5B17A241-BF36-48A6-BC29-4C32C08F5F94
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceGroup.md
ms.openlocfilehash: 0963d439efd4ab65a2117773cb6b7bb97043972c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663539"
---
# <span data-ttu-id="94f5f-101">Get-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="94f5f-101">Get-AzureRmResourceGroup</span></span>

## <span data-ttu-id="94f5f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="94f5f-102">SYNOPSIS</span></span>
<span data-ttu-id="94f5f-103">Ruft Ressourcengruppen ab.</span><span class="sxs-lookup"><span data-stu-id="94f5f-103">Gets resource groups.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="94f5f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="94f5f-104">SYNTAX</span></span>

### <span data-ttu-id="94f5f-105">Listet die Ressourcengruppe auf der Grundlage des Namens auf.</span><span class="sxs-lookup"><span data-stu-id="94f5f-105">Lists the resource group based on the name.</span></span> <span data-ttu-id="94f5f-106">Standard</span><span class="sxs-lookup"><span data-stu-id="94f5f-106">(Default)</span></span>
```
Get-AzureRmResourceGroup [-Name <String>] [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="94f5f-107">Listet die Ressourcengruppe auf der Grundlage der ID auf.</span><span class="sxs-lookup"><span data-stu-id="94f5f-107">Lists the resource group based on the Id.</span></span>
```
Get-AzureRmResourceGroup [-Location <String>] [-Id <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="94f5f-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="94f5f-108">DESCRIPTION</span></span>
<span data-ttu-id="94f5f-109">Das Cmdlet " **Get-AzureRmResourceGroup** " ruft Azure-Ressourcengruppen im aktuellen Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="94f5f-109">The **Get-AzureRmResourceGroup** cmdlet gets Azure resource groups in the current subscription.</span></span>
<span data-ttu-id="94f5f-110">Sie können alle Ressourcengruppen abrufen oder eine Ressourcengruppe nach Namen oder nach anderen Eigenschaften angeben.</span><span class="sxs-lookup"><span data-stu-id="94f5f-110">You can get all resource groups, or specify a resource group by name or by other properties.</span></span>
<span data-ttu-id="94f5f-111">Standardmäßig ruft dieses Cmdlet alle Ressourcengruppen im aktuellen Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="94f5f-111">By default, this cmdlet gets all resource groups in the current subscription.</span></span>

<span data-ttu-id="94f5f-112">Weitere Informationen zu Azure-Ressourcen und Azure-Ressourcengruppen finden Sie unter New-AzureRmResourceGroup-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="94f5f-112">For more information about Azure resources and Azure resource groups, see the New-AzureRmResourceGroup cmdlet.</span></span>

## <span data-ttu-id="94f5f-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="94f5f-113">EXAMPLES</span></span>

### <span data-ttu-id="94f5f-114">Beispiel 1: Abrufen einer Ressourcengruppe nach Namen</span><span class="sxs-lookup"><span data-stu-id="94f5f-114">Example 1: Get a resource group by name</span></span>
```
PS C:\>Get-AzureRmResourceGroup -Name "EngineerBlog"
```

<span data-ttu-id="94f5f-115">Dieser Befehl ruft die Azure-Ressourcengruppe in Ihrem Abonnement mit dem Namen EngineerBlog ab.</span><span class="sxs-lookup"><span data-stu-id="94f5f-115">This command gets the Azure resource group in your subscription named EngineerBlog.</span></span>

### <span data-ttu-id="94f5f-116">Beispiel 2: Abrufen aller Kategorien einer Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="94f5f-116">Example 2: Get all tags of a resource group</span></span>
```
PS C:\>(Get-AzureRmResourceGroup -Name "ContosoRG").Tags
```

<span data-ttu-id="94f5f-117">Dieser Befehl ruft die Ressourcengruppe mit dem Namen ContosoRG ab und zeigt die Tags an, die dieser Gruppe zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="94f5f-117">This command gets the resource group named ContosoRG, and displays the tags associated with that group.</span></span>

## <span data-ttu-id="94f5f-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="94f5f-118">PARAMETERS</span></span>

### <span data-ttu-id="94f5f-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="94f5f-119">-ApiVersion</span></span>
<span data-ttu-id="94f5f-120">Gibt die API-Version an, die vom Ressourcenanbieter unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="94f5f-120">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="94f5f-121">Sie können eine andere Version als die Standard Version angeben.</span><span class="sxs-lookup"><span data-stu-id="94f5f-121">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="94f5f-122">-ID</span><span class="sxs-lookup"><span data-stu-id="94f5f-122">-Id</span></span>
<span data-ttu-id="94f5f-123">Gibt die ID der Ressourcengruppe an, die abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="94f5f-123">Specifies the ID of the resource group to get.</span></span>
<span data-ttu-id="94f5f-124">Platzhalterzeichen sind nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="94f5f-124">Wildcard characters are not permitted.</span></span>

```yaml
Type: System.String
Parameter Sets: Lists the resource group based on the Id.
Aliases: ResourceGroupId, ResourceId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94f5f-125">-Standort</span><span class="sxs-lookup"><span data-stu-id="94f5f-125">-Location</span></span>
<span data-ttu-id="94f5f-126">Gibt den Speicherort der Ressourcengruppe an, die abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="94f5f-126">Specifies the location of the resource group to get.</span></span>

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

### <span data-ttu-id="94f5f-127">-Name</span><span class="sxs-lookup"><span data-stu-id="94f5f-127">-Name</span></span>
<span data-ttu-id="94f5f-128">Gibt den Namen der Ressourcengruppe an, die abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="94f5f-128">Specifies the name of the resource group to get.</span></span>
<span data-ttu-id="94f5f-129">Platzhalterzeichen sind nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="94f5f-129">Wildcard characters are not permitted.</span></span>

```yaml
Type: System.String
Parameter Sets: Lists the resource group based on the name.
Aliases: ResourceGroupName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94f5f-130">-Pre</span><span class="sxs-lookup"><span data-stu-id="94f5f-130">-Pre</span></span>
<span data-ttu-id="94f5f-131">Gibt an, dass dieses Cmdlet Pre-Release-API-Versionen berücksichtigt, wenn es automatisch die zu verwendende Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="94f5f-131">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="94f5f-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94f5f-132">-DefaultProfile</span></span>
<span data-ttu-id="94f5f-133">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="94f5f-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="94f5f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94f5f-134">CommonParameters</span></span>
<span data-ttu-id="94f5f-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94f5f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94f5f-136">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94f5f-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94f5f-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="94f5f-137">INPUTS</span></span>

### <span data-ttu-id="94f5f-138">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="94f5f-138">String</span></span>
<span data-ttu-id="94f5f-139">Sie können die Eingabe an das Cmdlet nach Eigenschaftsname, aber nicht nach Wert übergeben.</span><span class="sxs-lookup"><span data-stu-id="94f5f-139">You can pipe input to the cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="94f5f-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="94f5f-140">OUTPUTS</span></span>

### <span data-ttu-id="94f5f-141">Microsoft. Azure. Commands. ResourceManagement. PSResourceGroup</span><span class="sxs-lookup"><span data-stu-id="94f5f-141">Microsoft.Azure.Commands.ResourceManagement.PSResourceGroup</span></span>
<span data-ttu-id="94f5f-142">Dieses Cmdlet gibt Ressourcengruppen zurück.</span><span class="sxs-lookup"><span data-stu-id="94f5f-142">This cmdlet returns resource groups.</span></span>

## <span data-ttu-id="94f5f-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="94f5f-143">NOTES</span></span>

## <span data-ttu-id="94f5f-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="94f5f-144">RELATED LINKS</span></span>

[<span data-ttu-id="94f5f-145">Neu – AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="94f5f-145">New-AzureRmResourceGroup</span></span>](./New-AzureRmResourceGroup.md)

[<span data-ttu-id="94f5f-146">Remove-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="94f5f-146">Remove-AzureRmResourceGroup</span></span>](./Remove-AzureRmResourceGroup.md)

[<span data-ttu-id="94f5f-147">Satz-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="94f5f-147">Set-AzureRmResourceGroup</span></span>](./Set-AzureRmResourceGroup.md)


