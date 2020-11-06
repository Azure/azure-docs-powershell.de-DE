---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 60BED40A-EEA4-4667-93E9-8A9B35037726
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/move-azurermresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Move-AzureRmResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Move-AzureRmResource.md
ms.openlocfilehash: 4562c217a771f53995a531a3ca72066da672a144
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500421"
---
# <span data-ttu-id="29a2b-101">Move-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="29a2b-101">Move-AzureRmResource</span></span>

## <span data-ttu-id="29a2b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="29a2b-102">SYNOPSIS</span></span>
<span data-ttu-id="29a2b-103">Verschiebt eine Ressource in eine andere Ressourcengruppe oder ein anderes Abonnement.</span><span class="sxs-lookup"><span data-stu-id="29a2b-103">Moves a resource to a different resource group or subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="29a2b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="29a2b-104">SYNTAX</span></span>

```
Move-AzureRmResource -DestinationResourceGroupName <String> [-DestinationSubscriptionId <Guid>]
 -ResourceId <String[]> [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="29a2b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="29a2b-105">DESCRIPTION</span></span>
<span data-ttu-id="29a2b-106">Das Cmdlet **Move-AzureRmResource** verschiebt vorhandene Ressourcen in eine andere Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="29a2b-106">The **Move-AzureRmResource** cmdlet moves existing resources to a different resource group.</span></span>
<span data-ttu-id="29a2b-107">Diese Ressourcengruppe kann in einem anderen Abonnement enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="29a2b-107">That resource group can be in a different subscription.</span></span>

## <span data-ttu-id="29a2b-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="29a2b-108">EXAMPLES</span></span>

### <span data-ttu-id="29a2b-109">Beispiel 1: Verschieben einer Ressource in eine Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="29a2b-109">Example 1: Move a resource to a resource group</span></span>
```
PS C:\>$Resource = Get-AzureRmResource -ResourceType "Microsoft.ClassicCompute/storageAccounts" -ResourceName "ContosoStorageAccount"
PS C:\> Move-AzureRmResource -ResourceId $Resource.ResourceId -DestinationResourceGroupName "ResourceGroup14"
```

<span data-ttu-id="29a2b-110">Der erste Befehl ruft eine Ressource mit dem Namen ContosoStorageAccount mithilfe des Get-AzureRmResource-Cmdlets ab und speichert diese Ressource dann in der $Resource-Variablen.</span><span class="sxs-lookup"><span data-stu-id="29a2b-110">The first command gets a resource named ContosoStorageAccount by using the Get-AzureRmResource cmdlet, and then stores that resource in the $Resource variable.</span></span>

<span data-ttu-id="29a2b-111">Mit dem zweiten Befehl wird diese Ressource in die Ressourcengruppe mit dem Namen ResourceGroup14 verschoben.</span><span class="sxs-lookup"><span data-stu-id="29a2b-111">The second command moves that resource into the resource group named ResourceGroup14.</span></span>
<span data-ttu-id="29a2b-112">Der Befehl identifiziert die zu verschiebende Ressource mithilfe der Eigenschaft " **Resourcen** -Eigenschaft" von $Resource.</span><span class="sxs-lookup"><span data-stu-id="29a2b-112">The command identifies the resource to move by using the **ResourceId** property of $Resource.</span></span>

## <span data-ttu-id="29a2b-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="29a2b-113">PARAMETERS</span></span>

### <span data-ttu-id="29a2b-114">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="29a2b-114">-ApiVersion</span></span>
<span data-ttu-id="29a2b-115">Gibt die Version der zu verwendenden Ressourcenanbieter-API an.</span><span class="sxs-lookup"><span data-stu-id="29a2b-115">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="29a2b-116">Wenn Sie keine Version angeben, verwendet dieses Cmdlet die neueste verfügbare Version.</span><span class="sxs-lookup"><span data-stu-id="29a2b-116">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="29a2b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29a2b-117">-DefaultProfile</span></span>
<span data-ttu-id="29a2b-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="29a2b-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="29a2b-119">-DestinationResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29a2b-119">-DestinationResourceGroupName</span></span>
<span data-ttu-id="29a2b-120">Gibt den Namen der Ressourcengruppe an, in die das Cmdlet Ressourcen verschiebt.</span><span class="sxs-lookup"><span data-stu-id="29a2b-120">Specifies the name of the resource group into which this cmdlet moves resources.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: TargetResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29a2b-121">-DestinationSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="29a2b-121">-DestinationSubscriptionId</span></span>
<span data-ttu-id="29a2b-122">Gibt die ID des Abonnements an, in das dieses Cmdlet Ressourcen verschiebt.</span><span class="sxs-lookup"><span data-stu-id="29a2b-122">Specifies the ID of the subscription into which this cmdlet moves resources .</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: Id, SubscriptionId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29a2b-123">-Force</span><span class="sxs-lookup"><span data-stu-id="29a2b-123">-Force</span></span>
<span data-ttu-id="29a2b-124">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="29a2b-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="29a2b-125">-Information</span><span class="sxs-lookup"><span data-stu-id="29a2b-125">-InformationAction</span></span>
<span data-ttu-id="29a2b-126">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="29a2b-126">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="29a2b-127">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="29a2b-127">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="29a2b-128">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="29a2b-128">Continue</span></span>
- <span data-ttu-id="29a2b-129">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="29a2b-129">Ignore</span></span>
- <span data-ttu-id="29a2b-130">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="29a2b-130">Inquire</span></span>
- <span data-ttu-id="29a2b-131">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="29a2b-131">SilentlyContinue</span></span>
- <span data-ttu-id="29a2b-132">Beenden</span><span class="sxs-lookup"><span data-stu-id="29a2b-132">Stop</span></span>
- <span data-ttu-id="29a2b-133">Anhalten</span><span class="sxs-lookup"><span data-stu-id="29a2b-133">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29a2b-134">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="29a2b-134">-InformationVariable</span></span>
<span data-ttu-id="29a2b-135">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="29a2b-135">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29a2b-136">-Pre</span><span class="sxs-lookup"><span data-stu-id="29a2b-136">-Pre</span></span>
<span data-ttu-id="29a2b-137">Gibt an, dass dieses Cmdlet Pre-Release-API-Versionen berücksichtigt, wenn es automatisch die zu verwendende Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="29a2b-137">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="29a2b-138">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="29a2b-138">-ResourceId</span></span>
<span data-ttu-id="29a2b-139">Gibt ein Array von IDs der Ressourcen an, die dieses Cmdlet verschiebt.</span><span class="sxs-lookup"><span data-stu-id="29a2b-139">Specifies an array of IDs of the resources that this cmdlet moves.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="29a2b-140">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="29a2b-140">-Confirm</span></span>
<span data-ttu-id="29a2b-141">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="29a2b-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="29a2b-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29a2b-142">-WhatIf</span></span>
<span data-ttu-id="29a2b-143">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="29a2b-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="29a2b-144">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="29a2b-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="29a2b-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29a2b-145">CommonParameters</span></span>
<span data-ttu-id="29a2b-146">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29a2b-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29a2b-147">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29a2b-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29a2b-148">Eingaben</span><span class="sxs-lookup"><span data-stu-id="29a2b-148">INPUTS</span></span>

### <span data-ttu-id="29a2b-149">Zeichenfolge []</span><span class="sxs-lookup"><span data-stu-id="29a2b-149">String[]</span></span>
<span data-ttu-id="29a2b-150">Der Parameter ' resourcel ' akzeptiert den Wert vom Typ ' String [] ' aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="29a2b-150">Parameter 'ResourceId' accepts value of type 'String[]' from the pipeline</span></span>

## <span data-ttu-id="29a2b-151">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="29a2b-151">OUTPUTS</span></span>

### <span data-ttu-id="29a2b-152">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="29a2b-152">System.Boolean</span></span>

## <span data-ttu-id="29a2b-153">Notizen</span><span class="sxs-lookup"><span data-stu-id="29a2b-153">NOTES</span></span>

## <span data-ttu-id="29a2b-154">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="29a2b-154">RELATED LINKS</span></span>

[<span data-ttu-id="29a2b-155">Finden-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="29a2b-155">Find-AzureRmResource</span></span>](./Find-AzureRmResource.md)

[<span data-ttu-id="29a2b-156">Get-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="29a2b-156">Get-AzureRmResource</span></span>](./Get-AzureRmResource.md)

[<span data-ttu-id="29a2b-157">Neu – AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="29a2b-157">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="29a2b-158">Remove-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="29a2b-158">Remove-AzureRmResource</span></span>](./Remove-AzureRmResource.md)

[<span data-ttu-id="29a2b-159">Satz-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="29a2b-159">Set-AzureRmResource</span></span>](./Set-AzureRmResource.md)


