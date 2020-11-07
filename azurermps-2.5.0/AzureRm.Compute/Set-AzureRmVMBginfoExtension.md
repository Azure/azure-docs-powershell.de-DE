---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: B2B4E132-4A71-4DB8-A7B9-9ED3FE7EB292
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmbginfoextension
schema: 2.0.0
ms.openlocfilehash: 2d0b09e60872050ff1bad98b468763f69edfa723
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849691"
---
# <span data-ttu-id="2a54b-101">Set-AzureRmVMBginfoExtension</span><span class="sxs-lookup"><span data-stu-id="2a54b-101">Set-AzureRmVMBginfoExtension</span></span>

## <span data-ttu-id="2a54b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2a54b-102">SYNOPSIS</span></span>
<span data-ttu-id="2a54b-103">Fügt die BGInfo-Erweiterung zu einem virtuellen Computer hinzu.</span><span class="sxs-lookup"><span data-stu-id="2a54b-103">Adds the BGInfo extension to a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2a54b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2a54b-104">SYNTAX</span></span>

```
Set-AzureRmVMBginfoExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2a54b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2a54b-105">DESCRIPTION</span></span>
<span data-ttu-id="2a54b-106">Das Cmdlet " **Satz-AzureRmVMBGInfoExtension** " fügt die BGInfo-Erweiterung zu einem virtuellen Computer hinzu.</span><span class="sxs-lookup"><span data-stu-id="2a54b-106">The **Set-AzureRmVMBGInfoExtension** cmdlet adds the BGInfo extension to a virtual machine.</span></span>

## <span data-ttu-id="2a54b-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2a54b-107">EXAMPLES</span></span>

### <span data-ttu-id="2a54b-108">Beispiel 1: Hinzufügen der BGInfo-Erweiterung für einen virtuellen Computer</span><span class="sxs-lookup"><span data-stu-id="2a54b-108">Example 1: Add the BGInfo extension for a virtual machine</span></span>
```
PS C:\> Set-AzureVMBGInfoExtension -ResrouceGroupName "ContosoRG" -VMName "ContosoVM" -Name "ExtensionName" -TypeHandlerVersion "2.1" -Location "West Europe"
```

<span data-ttu-id="2a54b-109">Mit diesem Befehl wird die BGInfo-Erweiterung dem virtuellen Computer mit dem Namen ContosoVM hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="2a54b-109">This command adds the BGInfo extension to virtual machine named ContosoVM.</span></span>
<span data-ttu-id="2a54b-110">Der Befehl gibt die Ressourcengruppe und den Speicherort der virtuellen Maschine an.</span><span class="sxs-lookup"><span data-stu-id="2a54b-110">The command specifies the resource group and location of the virtual machine.</span></span>
<span data-ttu-id="2a54b-111">Der Befehl gibt den Namen und die Version der Erweiterung an.</span><span class="sxs-lookup"><span data-stu-id="2a54b-111">The command specifies the name and version of the extension.</span></span>

## <span data-ttu-id="2a54b-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="2a54b-112">PARAMETERS</span></span>

### <span data-ttu-id="2a54b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a54b-113">-DefaultProfile</span></span>
<span data-ttu-id="2a54b-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2a54b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2a54b-115">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="2a54b-115">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="2a54b-116">Gibt an, dass dieses Cmdlet verhindert, dass der Azure Guest-Agent die Erweiterung automatisch auf eine neuere Nebenversion aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="2a54b-116">Indicates that this cmdlet prevents the Azure guest agent from automatically updating the extension to a newer minor version.</span></span>
<span data-ttu-id="2a54b-117">Standardmäßig ermöglicht dieses Cmdlet dem Gast-Agent, die Erweiterung zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="2a54b-117">By default, this cmdlet enables the guest agent to update the extension.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a54b-118">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="2a54b-118">-ForceRerun</span></span>
<span data-ttu-id="2a54b-119">Gibt an, dass die Erweiterung erneut mit denselben öffentlichen oder geschützten Einstellungen ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="2a54b-119">Specifies that the extension should be run again with the same public or protected settings.</span></span>
<span data-ttu-id="2a54b-120">Der Wert kann eine beliebige Zeichenfolge sein, die vom aktuellen Wert abweicht.</span><span class="sxs-lookup"><span data-stu-id="2a54b-120">The value can be any string different from the current value.</span></span>

<span data-ttu-id="2a54b-121">Wenn forceUpdateTag nicht geändert wird, werden Updates für öffentliche oder geschützte Einstellungen weiterhin vom Handler angewendet.</span><span class="sxs-lookup"><span data-stu-id="2a54b-121">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a54b-122">-Standort</span><span class="sxs-lookup"><span data-stu-id="2a54b-122">-Location</span></span>
<span data-ttu-id="2a54b-123">Gibt den Speicherort der virtuellen Maschine an.</span><span class="sxs-lookup"><span data-stu-id="2a54b-123">Specifies the location of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a54b-124">-Name</span><span class="sxs-lookup"><span data-stu-id="2a54b-124">-Name</span></span>
<span data-ttu-id="2a54b-125">Gibt den Namen der BGInfo-Erweiterung an, die von diesem Cmdlet zu einem virtuellen Computer hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="2a54b-125">Specifies the name of the BGInfo extension that this cmdlet adds to a virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a54b-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a54b-126">-ResourceGroupName</span></span>
<span data-ttu-id="2a54b-127">Gibt den Namen der Ressourcengruppe des virtuellen Computers an, dem dieses Cmdlet eine Erweiterung hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="2a54b-127">Specifies the name of the resource group of the virtual machine to which this cmdlet adds an extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a54b-128">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="2a54b-128">-TypeHandlerVersion</span></span>
<span data-ttu-id="2a54b-129">Gibt die Version der Erweiterung an, die dieses Cmdlet dem virtuellen Computer hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="2a54b-129">Specifies the version of the extension that this cmdlet adds to the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a54b-130">-VMName</span><span class="sxs-lookup"><span data-stu-id="2a54b-130">-VMName</span></span>
<span data-ttu-id="2a54b-131">Gibt den Namen des virtuellen Computers an, dem dieses Cmdlet die BGInfo-Erweiterung hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="2a54b-131">Specifies the name of the virtual machine to which this cmdlet adds the BGInfo extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a54b-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2a54b-132">-Confirm</span></span>
<span data-ttu-id="2a54b-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2a54b-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2a54b-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a54b-134">-WhatIf</span></span>
<span data-ttu-id="2a54b-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2a54b-135">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="2a54b-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2a54b-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2a54b-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a54b-137">CommonParameters</span></span>
<span data-ttu-id="2a54b-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a54b-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a54b-139">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2a54b-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a54b-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2a54b-140">INPUTS</span></span>

### <span data-ttu-id="2a54b-141">Keine</span><span class="sxs-lookup"><span data-stu-id="2a54b-141">None</span></span>
<span data-ttu-id="2a54b-142">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="2a54b-142">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2a54b-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2a54b-143">OUTPUTS</span></span>

### <span data-ttu-id="2a54b-144">Microsoft. Azure. Commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="2a54b-144">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="2a54b-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="2a54b-145">NOTES</span></span>

## <span data-ttu-id="2a54b-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2a54b-146">RELATED LINKS</span></span>

