---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D93666EC-C252-4E3B-B311-50B6EEA6D4BF
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmaccessextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMAccessExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMAccessExtension.md
ms.openlocfilehash: 5eaf09aec561ed1fff37d2687253634bd1efc921
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93995617"
---
# <span data-ttu-id="a3bbf-101">Set-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="a3bbf-101">Set-AzVMAccessExtension</span></span>

## <span data-ttu-id="a3bbf-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a3bbf-102">SYNOPSIS</span></span>
<span data-ttu-id="a3bbf-103">Fügt die VMAccess-Erweiterung zu einem virtuellen Computer hinzu.</span><span class="sxs-lookup"><span data-stu-id="a3bbf-103">Adds the VMAccess extension to a virtual machine.</span></span>

## <span data-ttu-id="a3bbf-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a3bbf-104">SYNTAX</span></span>

```
Set-AzVMAccessExtension [-Credential <PSCredential>] [-ResourceGroupName] <String> [-VMName] <String>
 [-Name <String>] [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion]
 [-ForceRerun <String>] [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a3bbf-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a3bbf-105">DESCRIPTION</span></span>
<span data-ttu-id="a3bbf-106">Mit dem Cmdlet " **AzVMAccessExtension** " wird der Virtual Machine Access-VMAccess-VMAccess-Erweiterung zu einem virtuellen Computer hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="a3bbf-106">The **Set-AzVMAccessExtension** cmdlet adds the Virtual Machine Access (VMAccess) Virtual Machine VMAccess Extension to a virtual machine.</span></span> <span data-ttu-id="a3bbf-107">VMAccess Extension kann verwendet werden, um ein temporäres Kennwort festzulegen, das nach der Anmeldung am Computer sofort geändert werden sollte.</span><span class="sxs-lookup"><span data-stu-id="a3bbf-107">VMAccess Extension can be used to set a temporary password and this should be immediately changed it after logging into the machine.</span></span> <span data-ttu-id="a3bbf-108">Auf Windows-Domänencontrollern wird dies nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a3bbf-108">This is not supported on Windows Domain Controllers.</span></span>

## <span data-ttu-id="a3bbf-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a3bbf-109">EXAMPLES</span></span>

### <span data-ttu-id="a3bbf-110">Beispiel 1: Hinzufügen einer VMAccess-Erweiterung</span><span class="sxs-lookup"><span data-stu-id="a3bbf-110">Example 1: Add a VMAccess extension</span></span>
```
PS C:\> Set-AzVMAccessExtension -ResourceGroupName "ResourceGroup11" -Location "Central US" -VMName "VirtualMachine07" -Name "ContosoTest" -TypeHandlerVersion "2.4" -UserName "PFuller" -Password "Password"
```

<span data-ttu-id="a3bbf-111">Mit diesem Befehl wird eine VMAccess-Erweiterung für den virtuellen Computer mit dem Namen VirtualMachine07 in ResourceGroup11 hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="a3bbf-111">This command adds a VMAccess extension for the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>
<span data-ttu-id="a3bbf-112">Der Befehl gibt die Version für Name und Typ des Handlers für VMAccess an.</span><span class="sxs-lookup"><span data-stu-id="a3bbf-112">The command specifies the name and type handler version for VMAccess.</span></span>

## <span data-ttu-id="a3bbf-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="a3bbf-113">PARAMETERS</span></span>

### <span data-ttu-id="a3bbf-114">– Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="a3bbf-114">-Credential</span></span>
<span data-ttu-id="a3bbf-115">Gibt den Benutzernamen und das Kennwort für den virtuellen Computer als **PSCredential** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="a3bbf-115">Specifies the user name and password for the virtual machine as a **PSCredential** object.</span></span>
<span data-ttu-id="a3bbf-116">Wenn Sie einen anderen Namen als das aktuelle lokale Administratorkonto auf dem virtuellen Computer eingeben, fügt die VMAccess-Erweiterung ein lokales Administratorkonto mit diesem Namen hinzu und weist diesem Konto das angegebene Kennwort zu.</span><span class="sxs-lookup"><span data-stu-id="a3bbf-116">If you type a different name than the current local administrator account on your VM, the VMAccess extension will add a local administrator account with that name, and assign your specified password to that account.</span></span> <span data-ttu-id="a3bbf-117">Wenn das lokale Administratorkonto auf dem virtuellen Computer vorhanden ist, wird das Kennwort zurückgesetzt, und wenn das Konto deaktiviert ist, wird es durch die VMAccess-Erweiterung aktiviert.</span><span class="sxs-lookup"><span data-stu-id="a3bbf-117">If the local administrator account on your VM exists, it will reset the password and if the account is disabled, the VMAccess extension enables it.</span></span>
<span data-ttu-id="a3bbf-118">Verwenden Sie zum Abrufen von Anmeldeinformationen das Get-Credential-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a3bbf-118">To obtain a credential, use the Get-Credential cmdlet.</span></span>
<span data-ttu-id="a3bbf-119">Wenn Sie weitere Informationen wünschen, geben Sie `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="a3bbf-119">For more information, type `Get-Help Get-Credential`.</span></span>

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

### <span data-ttu-id="a3bbf-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3bbf-120">-DefaultProfile</span></span>
<span data-ttu-id="a3bbf-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a3bbf-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a3bbf-122">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="a3bbf-122">-DisableAutoUpgradeMinorVersion</span></span>
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

### <span data-ttu-id="a3bbf-123">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="a3bbf-123">-ForceRerun</span></span>
<span data-ttu-id="a3bbf-124">Gibt an, dass dieses Cmdlet eine erneute Ausführung derselben Erweiterungskonfiguration auf dem virtuellen Computer erzwingt, ohne die Erweiterung zu deinstallieren und erneut zu installieren.</span><span class="sxs-lookup"><span data-stu-id="a3bbf-124">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="a3bbf-125">Der Wert kann eine beliebige Zeichenfolge sein, die vom aktuellen Wert abweicht.</span><span class="sxs-lookup"><span data-stu-id="a3bbf-125">The value can be any string different from the current value.</span></span>
<span data-ttu-id="a3bbf-126">Wenn forceUpdateTag nicht geändert wird, werden Updates für öffentliche oder geschützte Einstellungen weiterhin vom Handler angewendet.</span><span class="sxs-lookup"><span data-stu-id="a3bbf-126">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="a3bbf-127">-Standort</span><span class="sxs-lookup"><span data-stu-id="a3bbf-127">-Location</span></span>
<span data-ttu-id="a3bbf-128">Gibt den Speicherort der virtuellen Maschine an.</span><span class="sxs-lookup"><span data-stu-id="a3bbf-128">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="a3bbf-129">-Name</span><span class="sxs-lookup"><span data-stu-id="a3bbf-129">-Name</span></span>
<span data-ttu-id="a3bbf-130">Gibt den Namen der Erweiterung an, die von diesem Cmdlet hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="a3bbf-130">Specifies the name of the extension that this cmdlet adds.</span></span>

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

### <span data-ttu-id="a3bbf-131">-Nowait</span><span class="sxs-lookup"><span data-stu-id="a3bbf-131">-NoWait</span></span>
<span data-ttu-id="a3bbf-132">Startet den Vorgang und gibt unmittelbar vor dem Abschluss des Vorgangs zurück.</span><span class="sxs-lookup"><span data-stu-id="a3bbf-132">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="a3bbf-133">Verwenden Sie einen anderen Mechanismus, um festzustellen, ob der Vorgang erfolgreich abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="a3bbf-133">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="a3bbf-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3bbf-134">-ResourceGroupName</span></span>
<span data-ttu-id="a3bbf-135">Gibt den Namen der Ressourcengruppe des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="a3bbf-135">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="a3bbf-136">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="a3bbf-136">-TypeHandlerVersion</span></span>
<span data-ttu-id="a3bbf-137">Gibt die Version der Erweiterung an, die für diesen virtuellen Computer verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="a3bbf-137">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="a3bbf-138">Führen Sie zum Abrufen der Version das Get-AzVMExtensionImage-Cmdlet mit dem Wert Microsoft. Compute für den *PublisherName* -Parameter und VMAccessAgent für den *Type* -Parameter aus.</span><span class="sxs-lookup"><span data-stu-id="a3bbf-138">To obtain the version, run the Get-AzVMExtensionImage cmdlet with a value of Microsoft.Compute for the *PublisherName* parameter and VMAccessAgent for the *Type* parameter.</span></span> <span data-ttu-id="a3bbf-139">Die typeHandlerVersion muss 2,0 oder größer sein, da Version 1 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="a3bbf-139">The typeHandlerVersion must be 2.0 or greater, as version 1 is deprecated.</span></span>

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

### <span data-ttu-id="a3bbf-140">-VMName</span><span class="sxs-lookup"><span data-stu-id="a3bbf-140">-VMName</span></span>
<span data-ttu-id="a3bbf-141">Gibt den Namen einer virtuellen Maschine an.</span><span class="sxs-lookup"><span data-stu-id="a3bbf-141">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="a3bbf-142">Dieses Cmdlet fügt dem virtuellen Computer, den dieser Parameter angibt, VMAccess hinzu.</span><span class="sxs-lookup"><span data-stu-id="a3bbf-142">This cmdlet adds VMAccess for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="a3bbf-143">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a3bbf-143">-Confirm</span></span>
<span data-ttu-id="a3bbf-144">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a3bbf-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a3bbf-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a3bbf-145">-WhatIf</span></span>
<span data-ttu-id="a3bbf-146">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a3bbf-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a3bbf-147">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a3bbf-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a3bbf-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3bbf-148">CommonParameters</span></span>
<span data-ttu-id="a3bbf-149">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3bbf-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3bbf-150">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a3bbf-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3bbf-151">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a3bbf-151">INPUTS</span></span>

### <span data-ttu-id="a3bbf-152">System. Management. Automation. PSCredential</span><span class="sxs-lookup"><span data-stu-id="a3bbf-152">System.Management.Automation.PSCredential</span></span>

### <span data-ttu-id="a3bbf-153">System. String</span><span class="sxs-lookup"><span data-stu-id="a3bbf-153">System.String</span></span>

### <span data-ttu-id="a3bbf-154">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="a3bbf-154">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="a3bbf-155">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a3bbf-155">OUTPUTS</span></span>

### <span data-ttu-id="a3bbf-156">Microsoft. Azure. Commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="a3bbf-156">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="a3bbf-157">Notizen</span><span class="sxs-lookup"><span data-stu-id="a3bbf-157">NOTES</span></span>

## <span data-ttu-id="a3bbf-158">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a3bbf-158">RELATED LINKS</span></span>

[<span data-ttu-id="a3bbf-159">Get-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="a3bbf-159">Get-AzVMAccessExtension</span></span>](./Get-AzVMAccessExtension.md)

[<span data-ttu-id="a3bbf-160">Remove-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="a3bbf-160">Remove-AzVMAccessExtension</span></span>](./Remove-AzVMAccessExtension.md)

[<span data-ttu-id="a3bbf-161">Satz-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="a3bbf-161">Set-AzVMExtension</span></span>](./Set-AzVMExtension.md)

[<span data-ttu-id="a3bbf-162">Get-AzVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="a3bbf-162">Get-AzVMExtensionImage</span></span>](./Get-AzVMExtensionImage.md)


