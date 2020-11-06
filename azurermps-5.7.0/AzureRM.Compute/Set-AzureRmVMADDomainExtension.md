---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 65BF37D3-4FCE-48A3-BC5D-01AA20FEB6CA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMADDomainExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMADDomainExtension.md
ms.openlocfilehash: b0af0f205f26862c20dd50e6181d2c11cd050dd1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93476929"
---
# <span data-ttu-id="4aabc-101">Set-AzureRmVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="4aabc-101">Set-AzureRmVMADDomainExtension</span></span>

## <span data-ttu-id="4aabc-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4aabc-102">SYNOPSIS</span></span>
<span data-ttu-id="4aabc-103">Fügt eine AD-Domänenerweiterung zu einem virtuellen Computer hinzu.</span><span class="sxs-lookup"><span data-stu-id="4aabc-103">Adds an AD domain extension to a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4aabc-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4aabc-104">SYNTAX</span></span>

```
Set-AzureRmVMADDomainExtension -DomainName <String> [-OUPath <String>] [-JoinOption <UInt32>]
 [-Credential <PSCredential>] [-Restart] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4aabc-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4aabc-105">DESCRIPTION</span></span>
<span data-ttu-id="4aabc-106">Das Cmdlet " **AzureRmVMADDomainExtension** " fügt einer virtuellen Maschine eine erweiterte Azure Active Directory (AD)-Domänenerweiterung hinzu.</span><span class="sxs-lookup"><span data-stu-id="4aabc-106">The **Set-AzureRmVMADDomainExtension** cmdlet adds an Azure Active Directory (AD) domain virtual machine extension to a virtual machine.</span></span>
<span data-ttu-id="4aabc-107">Diese Erweiterung ermöglicht dem virtuellen Computer, einer Domäne beizutreten.</span><span class="sxs-lookup"><span data-stu-id="4aabc-107">This extension lets your virtual machine join a domain.</span></span>

## <span data-ttu-id="4aabc-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4aabc-108">EXAMPLES</span></span>

## <span data-ttu-id="4aabc-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="4aabc-109">PARAMETERS</span></span>

### <span data-ttu-id="4aabc-110">– Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="4aabc-110">-Credential</span></span>
<span data-ttu-id="4aabc-111">Gibt den Benutzernamen und das Kennwort für den virtuellen Computer als **PSCredential** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="4aabc-111">Specifies the user name and password for the virtual machine as a **PSCredential** object.</span></span>
<span data-ttu-id="4aabc-112">Verwenden Sie zum Abrufen von Anmeldeinformationen das Get-Credential-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4aabc-112">To obtain a credential, use the Get-Credential cmdlet.</span></span>
<span data-ttu-id="4aabc-113">Wenn Sie weitere Informationen wünschen, geben Sie `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="4aabc-113">For more information, type `Get-Help Get-Credential`.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4aabc-114">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="4aabc-114">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="4aabc-115">Gibt an, dass dieses Cmdlet die automatische Aktualisierung der Nebenversion der Erweiterung deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="4aabc-115">Indicates that this cmdlet disables auto-upgrade of the minor version of the extension.</span></span>

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

### <span data-ttu-id="4aabc-116">-Domänenname</span><span class="sxs-lookup"><span data-stu-id="4aabc-116">-DomainName</span></span>
<span data-ttu-id="4aabc-117">Gibt den Namen der Domäne an.</span><span class="sxs-lookup"><span data-stu-id="4aabc-117">Specifies the name of the domain.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4aabc-118">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="4aabc-118">-ForceRerun</span></span>
<span data-ttu-id="4aabc-119">Gibt an, dass dieses Cmdlet eine erneute Ausführung derselben Erweiterungskonfiguration auf dem virtuellen Computer erzwingt, ohne die Erweiterung zu deinstallieren und erneut zu installieren.</span><span class="sxs-lookup"><span data-stu-id="4aabc-119">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="4aabc-120">Der Wert kann eine beliebige Zeichenfolge sein, die vom aktuellen Wert abweicht.</span><span class="sxs-lookup"><span data-stu-id="4aabc-120">The value can be any string different from the current value.</span></span>

<span data-ttu-id="4aabc-121">Wenn forceUpdateTag nicht geändert wird, werden Updates für öffentliche oder geschützte Einstellungen weiterhin vom Handler angewendet.</span><span class="sxs-lookup"><span data-stu-id="4aabc-121">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="4aabc-122">-JoinOption</span><span class="sxs-lookup"><span data-stu-id="4aabc-122">-JoinOption</span></span>
<span data-ttu-id="4aabc-123">Gibt die Join-Option an.</span><span class="sxs-lookup"><span data-stu-id="4aabc-123">Specifies the join option.</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4aabc-124">-Standort</span><span class="sxs-lookup"><span data-stu-id="4aabc-124">-Location</span></span>
<span data-ttu-id="4aabc-125">Gibt den Speicherort der virtuellen Maschine an.</span><span class="sxs-lookup"><span data-stu-id="4aabc-125">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="4aabc-126">-Name</span><span class="sxs-lookup"><span data-stu-id="4aabc-126">-Name</span></span>
<span data-ttu-id="4aabc-127">Gibt den Namen der hinzuzufügenden Domänenerweiterung an.</span><span class="sxs-lookup"><span data-stu-id="4aabc-127">Specifies the name of the domain extension to add.</span></span>

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

### <span data-ttu-id="4aabc-128">-OUPath</span><span class="sxs-lookup"><span data-stu-id="4aabc-128">-OUPath</span></span>
<span data-ttu-id="4aabc-129">Gibt eine Organisationseinheit (Organizational Unit, OU) für das Domänenkonto an.</span><span class="sxs-lookup"><span data-stu-id="4aabc-129">Specifies an organizational unit (OU) for the domain account.</span></span>
<span data-ttu-id="4aabc-130">Geben Sie den vollständigen Distinguished Name der OU in Anführungszeichen ein.</span><span class="sxs-lookup"><span data-stu-id="4aabc-130">Enter the full distinguished name of the OU in quotation marks.</span></span>
<span data-ttu-id="4aabc-131">Der Standardwert ist die standardmäßige OU für Machine-Objekte in der Domäne.</span><span class="sxs-lookup"><span data-stu-id="4aabc-131">The default value is the default OU for machine objects in the domain.</span></span>

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

### <span data-ttu-id="4aabc-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4aabc-132">-ResourceGroupName</span></span>
<span data-ttu-id="4aabc-133">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="4aabc-133">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="4aabc-134">-Neu starten</span><span class="sxs-lookup"><span data-stu-id="4aabc-134">-Restart</span></span>
<span data-ttu-id="4aabc-135">Gibt an, dass das Cmdlet den virtuellen Computer neu startet.</span><span class="sxs-lookup"><span data-stu-id="4aabc-135">Indicates that this cmdlet restarts the virtual machine.</span></span>
<span data-ttu-id="4aabc-136">Häufig ist ein Neustart erforderlich, um die Änderung effektiv zu gestalten.</span><span class="sxs-lookup"><span data-stu-id="4aabc-136">A restart is often required to make the change effective.</span></span>

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

### <span data-ttu-id="4aabc-137">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="4aabc-137">-TypeHandlerVersion</span></span>
<span data-ttu-id="4aabc-138">Gibt die Version der Domänenerweiterung an.</span><span class="sxs-lookup"><span data-stu-id="4aabc-138">Specifies the version of the domain extension.</span></span>

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

### <span data-ttu-id="4aabc-139">-VMName</span><span class="sxs-lookup"><span data-stu-id="4aabc-139">-VMName</span></span>
<span data-ttu-id="4aabc-140">Gibt den Namen der virtuellen Maschine an.</span><span class="sxs-lookup"><span data-stu-id="4aabc-140">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="4aabc-141">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="4aabc-141">-Confirm</span></span>
<span data-ttu-id="4aabc-142">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4aabc-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4aabc-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4aabc-143">-WhatIf</span></span>
<span data-ttu-id="4aabc-144">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4aabc-144">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="4aabc-145">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4aabc-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4aabc-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4aabc-146">CommonParameters</span></span>
<span data-ttu-id="4aabc-147">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4aabc-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4aabc-148">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4aabc-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4aabc-149">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4aabc-149">INPUTS</span></span>

### <span data-ttu-id="4aabc-150">Keine</span><span class="sxs-lookup"><span data-stu-id="4aabc-150">None</span></span>
<span data-ttu-id="4aabc-151">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="4aabc-151">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4aabc-152">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4aabc-152">OUTPUTS</span></span>

## <span data-ttu-id="4aabc-153">Notizen</span><span class="sxs-lookup"><span data-stu-id="4aabc-153">NOTES</span></span>

## <span data-ttu-id="4aabc-154">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4aabc-154">RELATED LINKS</span></span>

[<span data-ttu-id="4aabc-155">Get-AzureRmVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="4aabc-155">Get-AzureRmVMADDomainExtension</span></span>](./Get-AzureRmVMADDomainExtension.md)
