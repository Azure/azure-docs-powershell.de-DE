---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 65BF37D3-4FCE-48A3-BC5D-01AA20FEB6CA
online version: https://docs.microsoft.com/powershell/module/az.compute/set-azvmaddomainextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMADDomainExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMADDomainExtension.md
ms.openlocfilehash: 03f898246b2f0d784725488f753697ed893b09df
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101950315"
---
# <span data-ttu-id="1a0e3-101">Set-AzVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="1a0e3-101">Set-AzVMADDomainExtension</span></span>

## <span data-ttu-id="1a0e3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1a0e3-102">SYNOPSIS</span></span>
<span data-ttu-id="1a0e3-103">Fügt einem virtuellen Computer eine AD-Domänenerweiterung hinzu.</span><span class="sxs-lookup"><span data-stu-id="1a0e3-103">Adds an AD domain extension to a virtual machine.</span></span>

## <span data-ttu-id="1a0e3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1a0e3-104">SYNTAX</span></span>

```
Set-AzVMADDomainExtension -DomainName <String> [-OUPath <String>] [-JoinOption <UInt32>]
 [-Credential <PSCredential>] [-Restart] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1a0e3-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1a0e3-105">DESCRIPTION</span></span>
<span data-ttu-id="1a0e3-106">Das **Cmdlet Set-AzVMADDomainExtension** fügt einem virtuellen Computer eine Azure Active Directory (AD)-Domänenerweiterung hinzu.</span><span class="sxs-lookup"><span data-stu-id="1a0e3-106">The **Set-AzVMADDomainExtension** cmdlet adds an Azure Active Directory (AD) domain virtual machine extension to a virtual machine.</span></span>
<span data-ttu-id="1a0e3-107">Mit dieser Erweiterung kann Ihr virtueller Computer einer Domäne beitreten.</span><span class="sxs-lookup"><span data-stu-id="1a0e3-107">This extension lets your virtual machine join a domain.</span></span>

## <span data-ttu-id="1a0e3-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="1a0e3-108">EXAMPLES</span></span>

## <span data-ttu-id="1a0e3-109">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="1a0e3-109">PARAMETERS</span></span>

### <span data-ttu-id="1a0e3-110">-Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="1a0e3-110">-Credential</span></span>
<span data-ttu-id="1a0e3-111">Gibt den Benutzernamen und das Kennwort für den virtuellen Computer als **PSCredential-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="1a0e3-111">Specifies the user name and password for the virtual machine as a **PSCredential** object.</span></span>
<span data-ttu-id="1a0e3-112">Verwenden Sie das cmdlet Get-Credential, um eine Anmeldeinformationen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="1a0e3-112">To obtain a credential, use the Get-Credential cmdlet.</span></span>
<span data-ttu-id="1a0e3-113">Weitere Informationen finden Sie unter `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="1a0e3-113">For more information, type `Get-Help Get-Credential`.</span></span>

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

### <span data-ttu-id="1a0e3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a0e3-114">-DefaultProfile</span></span>
<span data-ttu-id="1a0e3-115">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1a0e3-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1a0e3-116">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="1a0e3-116">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="1a0e3-117">Gibt an, dass dieses Cmdlet das automatische Upgrade der Nebenversion der Erweiterung deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="1a0e3-117">Indicates that this cmdlet disables auto-upgrade of the minor version of the extension.</span></span>

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

### <span data-ttu-id="1a0e3-118">-DomainName</span><span class="sxs-lookup"><span data-stu-id="1a0e3-118">-DomainName</span></span>
<span data-ttu-id="1a0e3-119">Gibt den Namen der Domäne an.</span><span class="sxs-lookup"><span data-stu-id="1a0e3-119">Specifies the name of the domain.</span></span>

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

### <span data-ttu-id="1a0e3-120">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="1a0e3-120">-ForceRerun</span></span>
<span data-ttu-id="1a0e3-121">Gibt an, dass dieses Cmdlet eine Erneutes Ausführen derselben Erweiterungskonfiguration auf dem virtuellen Computer erzwingt, ohne die Erweiterung zu deinstallieren und erneut zu installieren.</span><span class="sxs-lookup"><span data-stu-id="1a0e3-121">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="1a0e3-122">Der Wert kann eine beliebige Zeichenfolge sein, die sich vom aktuellen Wert ab unterscheiden kann.</span><span class="sxs-lookup"><span data-stu-id="1a0e3-122">The value can be any string different from the current value.</span></span>
<span data-ttu-id="1a0e3-123">Wenn forceUpdateTag nicht geändert wird, werden Updates an öffentlichen oder geschützten Einstellungen weiterhin vom Handler angewendet.</span><span class="sxs-lookup"><span data-stu-id="1a0e3-123">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="1a0e3-124">-JoinOption</span><span class="sxs-lookup"><span data-stu-id="1a0e3-124">-JoinOption</span></span>
<span data-ttu-id="1a0e3-125">Gibt die Verknüpfungsoption an.</span><span class="sxs-lookup"><span data-stu-id="1a0e3-125">Specifies the join option.</span></span> <span data-ttu-id="1a0e3-126">Verknüpfungsoptionen finden Sie [unter fJoinOptions](https://docs.microsoft.com/windows/desktop/api/lmjoin/nf-lmjoin-netjoindomain)</span><span class="sxs-lookup"><span data-stu-id="1a0e3-126">For join options see [fJoinOptions](https://docs.microsoft.com/windows/desktop/api/lmjoin/nf-lmjoin-netjoindomain)</span></span>

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

### <span data-ttu-id="1a0e3-127">-Location</span><span class="sxs-lookup"><span data-stu-id="1a0e3-127">-Location</span></span>
<span data-ttu-id="1a0e3-128">Gibt den Speicherort des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="1a0e3-128">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="1a0e3-129">-Name</span><span class="sxs-lookup"><span data-stu-id="1a0e3-129">-Name</span></span>
<span data-ttu-id="1a0e3-130">Gibt den Namen der hinzuzufügenden Domänenerweiterung an.</span><span class="sxs-lookup"><span data-stu-id="1a0e3-130">Specifies the name of the domain extension to add.</span></span>

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

### <span data-ttu-id="1a0e3-131">-NoWait</span><span class="sxs-lookup"><span data-stu-id="1a0e3-131">-NoWait</span></span>
<span data-ttu-id="1a0e3-132">Startet den Vorgang und gibt sofort zurück, bevor der Vorgang abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="1a0e3-132">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="1a0e3-133">Verwenden Sie einen anderen Mechanismus, um festzustellen, ob der Vorgang erfolgreich abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="1a0e3-133">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="1a0e3-134">-OUPath</span><span class="sxs-lookup"><span data-stu-id="1a0e3-134">-OUPath</span></span>
<span data-ttu-id="1a0e3-135">Gibt eine Organisationseinheit (OU) für das Domänenkonto an.</span><span class="sxs-lookup"><span data-stu-id="1a0e3-135">Specifies an organizational unit (OU) for the domain account.</span></span>
<span data-ttu-id="1a0e3-136">Geben Sie den vollständigen Namen der Organisationseinheit in Anführungszeichen ein.</span><span class="sxs-lookup"><span data-stu-id="1a0e3-136">Enter the full distinguished name of the OU in quotation marks.</span></span>
<span data-ttu-id="1a0e3-137">Der Standardwert ist die Standard-OU für Computerobjekte in der Domäne.</span><span class="sxs-lookup"><span data-stu-id="1a0e3-137">The default value is the default OU for machine objects in the domain.</span></span>

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

### <span data-ttu-id="1a0e3-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a0e3-138">-ResourceGroupName</span></span>
<span data-ttu-id="1a0e3-139">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="1a0e3-139">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="1a0e3-140">-Neustart</span><span class="sxs-lookup"><span data-stu-id="1a0e3-140">-Restart</span></span>
<span data-ttu-id="1a0e3-141">Gibt an, dass mit diesem Cmdlet der virtuelle Computer neu gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="1a0e3-141">Indicates that this cmdlet restarts the virtual machine.</span></span>
<span data-ttu-id="1a0e3-142">Um die Änderung wirksam zu machen, ist häufig ein Neustart erforderlich.</span><span class="sxs-lookup"><span data-stu-id="1a0e3-142">A restart is often required to make the change effective.</span></span>

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

### <span data-ttu-id="1a0e3-143">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="1a0e3-143">-TypeHandlerVersion</span></span>
<span data-ttu-id="1a0e3-144">Gibt die Version der Domänenerweiterung an.</span><span class="sxs-lookup"><span data-stu-id="1a0e3-144">Specifies the version of the domain extension.</span></span>

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

### <span data-ttu-id="1a0e3-145">-VMName</span><span class="sxs-lookup"><span data-stu-id="1a0e3-145">-VMName</span></span>
<span data-ttu-id="1a0e3-146">Gibt den Namen des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="1a0e3-146">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="1a0e3-147">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1a0e3-147">-Confirm</span></span>
<span data-ttu-id="1a0e3-148">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1a0e3-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1a0e3-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1a0e3-149">-WhatIf</span></span>
<span data-ttu-id="1a0e3-150">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1a0e3-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1a0e3-151">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1a0e3-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1a0e3-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a0e3-152">CommonParameters</span></span>
<span data-ttu-id="1a0e3-153">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a0e3-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a0e3-154">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1a0e3-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a0e3-155">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="1a0e3-155">INPUTS</span></span>

### <span data-ttu-id="1a0e3-156">System.String</span><span class="sxs-lookup"><span data-stu-id="1a0e3-156">System.String</span></span>

### <span data-ttu-id="1a0e3-157">System.Nullable'1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="1a0e3-157">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="1a0e3-158">System.Management.Automation.PSCredential</span><span class="sxs-lookup"><span data-stu-id="1a0e3-158">System.Management.Automation.PSCredential</span></span>

### <span data-ttu-id="1a0e3-159">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="1a0e3-159">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="1a0e3-160">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="1a0e3-160">OUTPUTS</span></span>

### <span data-ttu-id="1a0e3-161">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="1a0e3-161">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="1a0e3-162">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="1a0e3-162">NOTES</span></span>

## <span data-ttu-id="1a0e3-163">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="1a0e3-163">RELATED LINKS</span></span>

[<span data-ttu-id="1a0e3-164">Get-AzVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="1a0e3-164">Get-AzVMADDomainExtension</span></span>](./Get-AzVMADDomainExtension.md)
