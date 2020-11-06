---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 65BF37D3-4FCE-48A3-BC5D-01AA20FEB6CA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmaddomainextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVMADDomainExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVMADDomainExtension.md
ms.openlocfilehash: e0d36e8ddc239d1d075b79e0c91df645d671c6a3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504461"
---
# <span data-ttu-id="67c9c-101">Set-AzureRmVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="67c9c-101">Set-AzureRmVMADDomainExtension</span></span>

## <span data-ttu-id="67c9c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="67c9c-102">SYNOPSIS</span></span>
<span data-ttu-id="67c9c-103">Fügt eine AD-Domänenerweiterung zu einem virtuellen Computer hinzu.</span><span class="sxs-lookup"><span data-stu-id="67c9c-103">Adds an AD domain extension to a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="67c9c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="67c9c-104">SYNTAX</span></span>

```
Set-AzureRmVMADDomainExtension -DomainName <String> [-OUPath <String>] [-JoinOption <UInt32>]
 [-Credential <PSCredential>] [-Restart] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="67c9c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="67c9c-105">DESCRIPTION</span></span>
<span data-ttu-id="67c9c-106">Das Cmdlet " **AzureRmVMADDomainExtension** " fügt einer virtuellen Maschine eine erweiterte Azure Active Directory (AD)-Domänenerweiterung hinzu.</span><span class="sxs-lookup"><span data-stu-id="67c9c-106">The **Set-AzureRmVMADDomainExtension** cmdlet adds an Azure Active Directory (AD) domain virtual machine extension to a virtual machine.</span></span>
<span data-ttu-id="67c9c-107">Diese Erweiterung ermöglicht dem virtuellen Computer, einer Domäne beizutreten.</span><span class="sxs-lookup"><span data-stu-id="67c9c-107">This extension lets your virtual machine join a domain.</span></span>

## <span data-ttu-id="67c9c-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="67c9c-108">EXAMPLES</span></span>

## <span data-ttu-id="67c9c-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="67c9c-109">PARAMETERS</span></span>

### <span data-ttu-id="67c9c-110">– Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="67c9c-110">-Credential</span></span>
<span data-ttu-id="67c9c-111">Gibt den Benutzernamen und das Kennwort für den virtuellen Computer als **PSCredential** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="67c9c-111">Specifies the user name and password for the virtual machine as a **PSCredential** object.</span></span>
<span data-ttu-id="67c9c-112">Verwenden Sie zum Abrufen von Anmeldeinformationen das Get-Credential-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="67c9c-112">To obtain a credential, use the Get-Credential cmdlet.</span></span>
<span data-ttu-id="67c9c-113">Wenn Sie weitere Informationen wünschen, geben Sie `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="67c9c-113">For more information, type `Get-Help Get-Credential`.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67c9c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67c9c-114">-DefaultProfile</span></span>
<span data-ttu-id="67c9c-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="67c9c-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="67c9c-116">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="67c9c-116">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="67c9c-117">Gibt an, dass dieses Cmdlet die automatische Aktualisierung der Nebenversion der Erweiterung deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="67c9c-117">Indicates that this cmdlet disables auto-upgrade of the minor version of the extension.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67c9c-118">-Domänenname</span><span class="sxs-lookup"><span data-stu-id="67c9c-118">-DomainName</span></span>
<span data-ttu-id="67c9c-119">Gibt den Namen der Domäne an.</span><span class="sxs-lookup"><span data-stu-id="67c9c-119">Specifies the name of the domain.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67c9c-120">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="67c9c-120">-ForceRerun</span></span>
<span data-ttu-id="67c9c-121">Gibt an, dass dieses Cmdlet eine erneute Ausführung derselben Erweiterungskonfiguration auf dem virtuellen Computer erzwingt, ohne die Erweiterung zu deinstallieren und erneut zu installieren.</span><span class="sxs-lookup"><span data-stu-id="67c9c-121">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="67c9c-122">Der Wert kann eine beliebige Zeichenfolge sein, die vom aktuellen Wert abweicht.</span><span class="sxs-lookup"><span data-stu-id="67c9c-122">The value can be any string different from the current value.</span></span>
<span data-ttu-id="67c9c-123">Wenn forceUpdateTag nicht geändert wird, werden Updates für öffentliche oder geschützte Einstellungen weiterhin vom Handler angewendet.</span><span class="sxs-lookup"><span data-stu-id="67c9c-123">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="67c9c-124">-JoinOption</span><span class="sxs-lookup"><span data-stu-id="67c9c-124">-JoinOption</span></span>
<span data-ttu-id="67c9c-125">Gibt die Join-Option an.</span><span class="sxs-lookup"><span data-stu-id="67c9c-125">Specifies the join option.</span></span> <span data-ttu-id="67c9c-126">Informationen zu Verknüpfungsoptionen finden Sie unter [fJoinOptions](https://docs.microsoft.com/en-us/windows/desktop/api/lmjoin/nf-lmjoin-netjoindomain)</span><span class="sxs-lookup"><span data-stu-id="67c9c-126">For join options see [fJoinOptions](https://docs.microsoft.com/en-us/windows/desktop/api/lmjoin/nf-lmjoin-netjoindomain)</span></span>

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67c9c-127">-Standort</span><span class="sxs-lookup"><span data-stu-id="67c9c-127">-Location</span></span>
<span data-ttu-id="67c9c-128">Gibt den Speicherort der virtuellen Maschine an.</span><span class="sxs-lookup"><span data-stu-id="67c9c-128">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="67c9c-129">-Name</span><span class="sxs-lookup"><span data-stu-id="67c9c-129">-Name</span></span>
<span data-ttu-id="67c9c-130">Gibt den Namen der hinzuzufügenden Domänenerweiterung an.</span><span class="sxs-lookup"><span data-stu-id="67c9c-130">Specifies the name of the domain extension to add.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67c9c-131">-OUPath</span><span class="sxs-lookup"><span data-stu-id="67c9c-131">-OUPath</span></span>
<span data-ttu-id="67c9c-132">Gibt eine Organisationseinheit (Organizational Unit, OU) für das Domänenkonto an.</span><span class="sxs-lookup"><span data-stu-id="67c9c-132">Specifies an organizational unit (OU) for the domain account.</span></span>
<span data-ttu-id="67c9c-133">Geben Sie den vollständigen Distinguished Name der OU in Anführungszeichen ein.</span><span class="sxs-lookup"><span data-stu-id="67c9c-133">Enter the full distinguished name of the OU in quotation marks.</span></span>
<span data-ttu-id="67c9c-134">Der Standardwert ist die standardmäßige OU für Machine-Objekte in der Domäne.</span><span class="sxs-lookup"><span data-stu-id="67c9c-134">The default value is the default OU for machine objects in the domain.</span></span>

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

### <span data-ttu-id="67c9c-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67c9c-135">-ResourceGroupName</span></span>
<span data-ttu-id="67c9c-136">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="67c9c-136">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67c9c-137">-Neu starten</span><span class="sxs-lookup"><span data-stu-id="67c9c-137">-Restart</span></span>
<span data-ttu-id="67c9c-138">Gibt an, dass das Cmdlet den virtuellen Computer neu startet.</span><span class="sxs-lookup"><span data-stu-id="67c9c-138">Indicates that this cmdlet restarts the virtual machine.</span></span>
<span data-ttu-id="67c9c-139">Häufig ist ein Neustart erforderlich, um die Änderung effektiv zu gestalten.</span><span class="sxs-lookup"><span data-stu-id="67c9c-139">A restart is often required to make the change effective.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67c9c-140">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="67c9c-140">-TypeHandlerVersion</span></span>
<span data-ttu-id="67c9c-141">Gibt die Version der Domänenerweiterung an.</span><span class="sxs-lookup"><span data-stu-id="67c9c-141">Specifies the version of the domain extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67c9c-142">-VMName</span><span class="sxs-lookup"><span data-stu-id="67c9c-142">-VMName</span></span>
<span data-ttu-id="67c9c-143">Gibt den Namen der virtuellen Maschine an.</span><span class="sxs-lookup"><span data-stu-id="67c9c-143">Specifies the name of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67c9c-144">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="67c9c-144">-Confirm</span></span>
<span data-ttu-id="67c9c-145">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="67c9c-145">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67c9c-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67c9c-146">-WhatIf</span></span>
<span data-ttu-id="67c9c-147">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="67c9c-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="67c9c-148">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="67c9c-148">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67c9c-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67c9c-149">CommonParameters</span></span>
<span data-ttu-id="67c9c-150">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67c9c-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67c9c-151">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67c9c-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67c9c-152">Eingaben</span><span class="sxs-lookup"><span data-stu-id="67c9c-152">INPUTS</span></span>

### <span data-ttu-id="67c9c-153">System. String</span><span class="sxs-lookup"><span data-stu-id="67c9c-153">System.String</span></span>

### <span data-ttu-id="67c9c-154">System. Nullable ' 1 [[System. UInt32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="67c9c-154">System.Nullable\`1[[System.UInt32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="67c9c-155">System. Management. Automation. PSCredential</span><span class="sxs-lookup"><span data-stu-id="67c9c-155">System.Management.Automation.PSCredential</span></span>

### <span data-ttu-id="67c9c-156">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="67c9c-156">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="67c9c-157">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="67c9c-157">OUTPUTS</span></span>

### <span data-ttu-id="67c9c-158">Microsoft. Azure. Commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="67c9c-158">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="67c9c-159">Notizen</span><span class="sxs-lookup"><span data-stu-id="67c9c-159">NOTES</span></span>

## <span data-ttu-id="67c9c-160">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="67c9c-160">RELATED LINKS</span></span>

[<span data-ttu-id="67c9c-161">Get-AzureRmVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="67c9c-161">Get-AzureRmVMADDomainExtension</span></span>](./Get-AzureRmVMADDomainExtension.md)
