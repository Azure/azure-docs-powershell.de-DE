---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: D93666EC-C252-4E3B-B311-50B6EEA6D4BF
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmaccessextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMAccessExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMAccessExtension.md
ms.openlocfilehash: b0335a063e810a94e6d557986e682ec4c777e5c1
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844251"
---
# <span data-ttu-id="f7c8a-101">Set-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="f7c8a-101">Set-AzVMAccessExtension</span></span>

## <span data-ttu-id="f7c8a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f7c8a-102">SYNOPSIS</span></span>
<span data-ttu-id="f7c8a-103">Fügt die VMAccess-Erweiterung zu einem virtuellen Computer hinzu.</span><span class="sxs-lookup"><span data-stu-id="f7c8a-103">Adds the VMAccess extension to a virtual machine.</span></span>

## <span data-ttu-id="f7c8a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f7c8a-104">SYNTAX</span></span>

```
Set-AzVMAccessExtension [-Credential <PSCredential>] [-ResourceGroupName] <String> [-VMName] <String>
 [-Name <String>] [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion]
 [-ForceRerun <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f7c8a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f7c8a-105">DESCRIPTION</span></span>
<span data-ttu-id="f7c8a-106">Mit dem Cmdlet " **AzVMAccessExtension** " wird der Virtual Machine Access-VMAccess-VMAccess-Erweiterung zu einem virtuellen Computer hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="f7c8a-106">The **Set-AzVMAccessExtension** cmdlet adds the Virtual Machine Access (VMAccess) Virtual Machine VMAccess Extension to a virtual machine.</span></span> <span data-ttu-id="f7c8a-107">VMAccess Extension kann verwendet werden, um ein temporäres Kennwort festzulegen, das nach der Anmeldung am Computer sofort geändert werden sollte.</span><span class="sxs-lookup"><span data-stu-id="f7c8a-107">VMAccess Extension can be used to set a temporary password and this should be immediately changed it after logging into the machine.</span></span>

## <span data-ttu-id="f7c8a-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f7c8a-108">EXAMPLES</span></span>

### <span data-ttu-id="f7c8a-109">Beispiel 1: Hinzufügen einer VMAccess-Erweiterung</span><span class="sxs-lookup"><span data-stu-id="f7c8a-109">Example 1: Add a VMAccess extension</span></span>
```
PS C:\> Set-AzVMAccessExtension -ResourceGroupName "ResrouceGroup11" -Location "Central US" -VMName "VirtualMachine07" -Name "ContosoTest" -TypeHandlerVersion "2.0" -UserName "PFuller" -Password "Password"
```

<span data-ttu-id="f7c8a-110">Mit diesem Befehl wird eine VMAccess-Erweiterung für den virtuellen Computer mit dem Namen VirtualMachine07 in ResrouceGroup11 hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="f7c8a-110">This command adds a VMAccess extension for the virtual machine named VirtualMachine07 in ResrouceGroup11.</span></span>
<span data-ttu-id="f7c8a-111">Der Befehl gibt die Version für Name und Typ des Handlers für VMAccess an.</span><span class="sxs-lookup"><span data-stu-id="f7c8a-111">The command specifies the name and type handler version for VMAccess.</span></span>

## <span data-ttu-id="f7c8a-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="f7c8a-112">PARAMETERS</span></span>

### <span data-ttu-id="f7c8a-113">– Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="f7c8a-113">-Credential</span></span>
<span data-ttu-id="f7c8a-114">Gibt den Benutzernamen und das Kennwort für den virtuellen Computer als **PSCredential** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="f7c8a-114">Specifies the user name and password for the virtual machine as a **PSCredential** object.</span></span>
<span data-ttu-id="f7c8a-115">Verwenden Sie zum Abrufen von Anmeldeinformationen das Get-Credential-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f7c8a-115">To obtain a credential, use the Get-Credential cmdlet.</span></span>
<span data-ttu-id="f7c8a-116">Wenn Sie weitere Informationen wünschen, geben Sie `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="f7c8a-116">For more information, type `Get-Help Get-Credential`.</span></span>

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

### <span data-ttu-id="f7c8a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7c8a-117">-DefaultProfile</span></span>
<span data-ttu-id="f7c8a-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f7c8a-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f7c8a-119">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="f7c8a-119">-DisableAutoUpgradeMinorVersion</span></span>
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

### <span data-ttu-id="f7c8a-120">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="f7c8a-120">-ForceRerun</span></span>
<span data-ttu-id="f7c8a-121">Gibt an, dass dieses Cmdlet eine erneute Ausführung derselben Erweiterungskonfiguration auf dem virtuellen Computer erzwingt, ohne die Erweiterung zu deinstallieren und erneut zu installieren.</span><span class="sxs-lookup"><span data-stu-id="f7c8a-121">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="f7c8a-122">Der Wert kann eine beliebige Zeichenfolge sein, die vom aktuellen Wert abweicht.</span><span class="sxs-lookup"><span data-stu-id="f7c8a-122">The value can be any string different from the current value.</span></span>

<span data-ttu-id="f7c8a-123">Wenn forceUpdateTag nicht geändert wird, werden Updates für öffentliche oder geschützte Einstellungen weiterhin vom Handler angewendet.</span><span class="sxs-lookup"><span data-stu-id="f7c8a-123">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="f7c8a-124">-Standort</span><span class="sxs-lookup"><span data-stu-id="f7c8a-124">-Location</span></span>
<span data-ttu-id="f7c8a-125">Gibt den Speicherort der virtuellen Maschine an.</span><span class="sxs-lookup"><span data-stu-id="f7c8a-125">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="f7c8a-126">-Name</span><span class="sxs-lookup"><span data-stu-id="f7c8a-126">-Name</span></span>
<span data-ttu-id="f7c8a-127">Gibt den Namen der Erweiterung an, die von diesem Cmdlet hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="f7c8a-127">Specifies the name of the extension that this cmdlet adds.</span></span>

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

### <span data-ttu-id="f7c8a-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7c8a-128">-ResourceGroupName</span></span>
<span data-ttu-id="f7c8a-129">Gibt den Namen der Ressourcengruppe des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="f7c8a-129">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="f7c8a-130">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="f7c8a-130">-TypeHandlerVersion</span></span>
<span data-ttu-id="f7c8a-131">Gibt die Version der Erweiterung an, die für diesen virtuellen Computer verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="f7c8a-131">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="f7c8a-132">Führen Sie zum Abrufen der Version das Get-AzVMExtensionImage-Cmdlet mit dem Wert Microsoft. Compute für den *PublisherName* -Parameter und VMAccessAgent für den *Type* -Parameter aus.</span><span class="sxs-lookup"><span data-stu-id="f7c8a-132">To obtain the version, run the Get-AzVMExtensionImage cmdlet with a value of Microsoft.Compute for the *PublisherName* parameter and VMAccessAgent for the *Type* parameter.</span></span>

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

### <span data-ttu-id="f7c8a-133">-VMName</span><span class="sxs-lookup"><span data-stu-id="f7c8a-133">-VMName</span></span>
<span data-ttu-id="f7c8a-134">Gibt den Namen einer virtuellen Maschine an.</span><span class="sxs-lookup"><span data-stu-id="f7c8a-134">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="f7c8a-135">Dieses Cmdlet fügt dem virtuellen Computer, den dieser Parameter angibt, VMAccess hinzu.</span><span class="sxs-lookup"><span data-stu-id="f7c8a-135">This cmdlet adds VMAccess for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="f7c8a-136">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f7c8a-136">-Confirm</span></span>
<span data-ttu-id="f7c8a-137">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f7c8a-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f7c8a-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7c8a-138">-WhatIf</span></span>
<span data-ttu-id="f7c8a-139">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f7c8a-139">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="f7c8a-140">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f7c8a-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f7c8a-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7c8a-141">CommonParameters</span></span>
<span data-ttu-id="f7c8a-142">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7c8a-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7c8a-143">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f7c8a-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7c8a-144">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f7c8a-144">INPUTS</span></span>

### <span data-ttu-id="f7c8a-145">Keine</span><span class="sxs-lookup"><span data-stu-id="f7c8a-145">None</span></span>
<span data-ttu-id="f7c8a-146">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="f7c8a-146">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f7c8a-147">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f7c8a-147">OUTPUTS</span></span>

### <span data-ttu-id="f7c8a-148">Microsoft. Azure. Commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="f7c8a-148">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="f7c8a-149">Notizen</span><span class="sxs-lookup"><span data-stu-id="f7c8a-149">NOTES</span></span>

## <span data-ttu-id="f7c8a-150">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f7c8a-150">RELATED LINKS</span></span>

[<span data-ttu-id="f7c8a-151">Get-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="f7c8a-151">Get-AzVMAccessExtension</span></span>](./Get-AzVMAccessExtension.md)

[<span data-ttu-id="f7c8a-152">Remove-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="f7c8a-152">Remove-AzVMAccessExtension</span></span>](./Remove-AzVMAccessExtension.md)

[<span data-ttu-id="f7c8a-153">Satz-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="f7c8a-153">Set-AzVMExtension</span></span>](./Set-AzVMExtension.md)

[<span data-ttu-id="f7c8a-154">Get-AzVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="f7c8a-154">Get-AzVMExtensionImage</span></span>](./Get-AzVMExtensionImage.md)


