---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 50B64FFE-8277-4DAA-805A-271123B35355
online version: https://docs.microsoft.com/powershell/module/az.compute/add-azvmadditionalunattendcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMAdditionalUnattendContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMAdditionalUnattendContent.md
ms.openlocfilehash: 2ec50d8e0c11143f72e327a7b73784c1a49e926c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101938912"
---
# <span data-ttu-id="a3438-101">Add-AzVMAdditionalUnattendContent</span><span class="sxs-lookup"><span data-stu-id="a3438-101">Add-AzVMAdditionalUnattendContent</span></span>

## <span data-ttu-id="a3438-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a3438-102">SYNOPSIS</span></span>
<span data-ttu-id="a3438-103">Fügt der unbeaufsichtigten Windows Setup-Antwortdatei Informationen hinzu.</span><span class="sxs-lookup"><span data-stu-id="a3438-103">Adds information to the unattended Windows Setup answer file.</span></span>

## <span data-ttu-id="a3438-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a3438-104">SYNTAX</span></span>

```
Add-AzVMAdditionalUnattendContent [-VM] <PSVirtualMachine> [[-Content] <String>]
 [[-SettingName] <SettingNames>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a3438-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a3438-105">DESCRIPTION</span></span>
<span data-ttu-id="a3438-106">Das **Cmdlet Add-AzVMAdditionalUnattendContent** fügt der unbeaufsichtigten Windows Setup-Antwortdatei Informationen hinzu.</span><span class="sxs-lookup"><span data-stu-id="a3438-106">The **Add-AzVMAdditionalUnattendContent** cmdlet adds information to the unattended Windows Setup answer file.</span></span>
<span data-ttu-id="a3438-107">Geben Sie zusätzliche xml-formatierte Basisinformationen an, die von diesem Cmdlet zur unattend.xml werden.</span><span class="sxs-lookup"><span data-stu-id="a3438-107">Specify additional base 64 encoded .xml formatted information that this cmdlet adds to the unattend.xml file.</span></span>

## <span data-ttu-id="a3438-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a3438-108">EXAMPLES</span></span>

### <span data-ttu-id="a3438-109">Beispiel 1: Hinzufügen von Inhalt zu unattend.xml</span><span class="sxs-lookup"><span data-stu-id="a3438-109">Example 1: Add content to unattend.xml</span></span>
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id 
PS C:\> $Credential = Get-Credential
PS C:\> $VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine  -Windows -ComputerName "Contoso26" -Credential $Credential
PS C:\> $AucContent = "<UserAccounts><AdministratorPassword><Value>" + "Password" + "</Value><PlainText>true</PlainText></AdministratorPassword></UserAccounts>";
PS C:\> $VirtualMachine = Add-AzVMAdditionalUnattendContent -VM $VirtualMachine -Content $AucContent -SettingName "AutoLogon"
```

<span data-ttu-id="a3438-110">Der erste Befehl ruft den Verfügbarkeitssatz "AvailabilitySet03" in der Ressourcengruppe "ResourceGroup11" ab und speichert dieses Objekt dann in der $AvailabilitySet Variablen.</span><span class="sxs-lookup"><span data-stu-id="a3438-110">The first command gets the availability set named AvailabilitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="a3438-111">Mit dem zweiten Befehl wird ein Objekt eines virtuellen Computers erstellt und dann in der $VirtualMachine gespeichert.</span><span class="sxs-lookup"><span data-stu-id="a3438-111">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="a3438-112">Der Befehl weist dem virtuellen Computer einen Namen und eine Größe zu.</span><span class="sxs-lookup"><span data-stu-id="a3438-112">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="a3438-113">Der virtuelle Computer gehört zu dem Verfügbarkeitssatz, der auf der $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="a3438-113">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="a3438-114">Der dritte Befehl erstellt ein Anmeldeinformationsobjekt mithilfe des cmdlets Get-Credential und speichert dann das Ergebnis in der $Credential Variablen.</span><span class="sxs-lookup"><span data-stu-id="a3438-114">The third command creates a credential object by using the Get-Credential cmdlet, and then stores the result in the $Credential variable.</span></span>
<span data-ttu-id="a3438-115">Mit dem Befehl werden Sie aufgefordert, einen Benutzernamen und ein Kennwort einzugeben.</span><span class="sxs-lookup"><span data-stu-id="a3438-115">The command prompts you for a user name and password.</span></span>
<span data-ttu-id="a3438-116">Weitere Informationen finden Sie unter `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="a3438-116">For more information, type `Get-Help Get-Credential`.</span></span>
<span data-ttu-id="a3438-117">Der vierte Befehl verwendet das **Set-AzVMOperatingSystem-Cmdlet,** um den virtuellen Computer zu konfigurieren, der auf einem $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="a3438-117">The fourth command uses the **Set-AzVMOperatingSystem** cmdlet to configure the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="a3438-118">Der fünfte Befehl weist der Variablen inhalt $AucContent zu.</span><span class="sxs-lookup"><span data-stu-id="a3438-118">The fifth command assigns content to the $AucContent variable.</span></span>
<span data-ttu-id="a3438-119">Der Inhalt enthält ein Kennwort.</span><span class="sxs-lookup"><span data-stu-id="a3438-119">The content includes a password.</span></span>
<span data-ttu-id="a3438-120">Der letzte Befehl fügt den in der Datei gespeicherten $AucContent der datei unattend.xml hinzu.</span><span class="sxs-lookup"><span data-stu-id="a3438-120">The final command adds the content stored in $AucContent to the unattend.xml file.</span></span>

## <span data-ttu-id="a3438-121">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="a3438-121">PARAMETERS</span></span>

### <span data-ttu-id="a3438-122">-Inhalt</span><span class="sxs-lookup"><span data-stu-id="a3438-122">-Content</span></span>
<span data-ttu-id="a3438-123">Gibt basis-64-codierten XML-formatierten Inhalt an.</span><span class="sxs-lookup"><span data-stu-id="a3438-123">Specifies base 64 encoded XML formatted content.</span></span>
<span data-ttu-id="a3438-124">Dieses Cmdlet fügt den Inhalt der datei unattend.xml hinzu.</span><span class="sxs-lookup"><span data-stu-id="a3438-124">This cmdlet adds the content to the unattend.xml file.</span></span>
<span data-ttu-id="a3438-125">Der XML-Inhalt muss kleiner als 4 KB sein und das Stammelement für die Einstellung oder das Feature enthalten, das von diesem Cmdlet eingefügt wird.</span><span class="sxs-lookup"><span data-stu-id="a3438-125">The XML content must be less than 4 KB and must include the root element for the setting or feature that this cmdlet inserts.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3438-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3438-126">-DefaultProfile</span></span>
<span data-ttu-id="a3438-127">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a3438-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a3438-128">-SettingName</span><span class="sxs-lookup"><span data-stu-id="a3438-128">-SettingName</span></span>
<span data-ttu-id="a3438-129">Gibt den Namen der Einstellung an, auf die der Inhalt angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="a3438-129">Specifies the name of the setting to which the content applies.</span></span>
<span data-ttu-id="a3438-130">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="a3438-130">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a3438-131">FirstLogonCommands</span><span class="sxs-lookup"><span data-stu-id="a3438-131">FirstLogonCommands</span></span>
- <span data-ttu-id="a3438-132">AutoLogon</span><span class="sxs-lookup"><span data-stu-id="a3438-132">AutoLogon</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.SettingNames]
Parameter Sets: (All)
Aliases:
Accepted values: AutoLogon, FirstLogonCommands

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3438-133">-VM</span><span class="sxs-lookup"><span data-stu-id="a3438-133">-VM</span></span>
<span data-ttu-id="a3438-134">Gibt das Objekt des virtuellen Computers an, das von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="a3438-134">Specifies the virtual machine object that this cmdlet modifies.</span></span>
<span data-ttu-id="a3438-135">Zum Abrufen eines Virtuellen Computerobjekts verwenden Sie [das Get-AzVM-Cmdlet.](./Get-AzVM.md)</span><span class="sxs-lookup"><span data-stu-id="a3438-135">To obtain a virtual machine object, use the [Get-AzVM](./Get-AzVM.md) cmdlet.</span></span>
<span data-ttu-id="a3438-136">Erstellen Sie ein Objekt eines virtuellen Computers mithilfe des [Cmdlets New-AzVMConfig.](./New-AzVMConfig.md)</span><span class="sxs-lookup"><span data-stu-id="a3438-136">Create a virtual machine object by using the [New-AzVMConfig](./New-AzVMConfig.md) cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a3438-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3438-137">CommonParameters</span></span>
<span data-ttu-id="a3438-138">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3438-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3438-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a3438-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3438-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a3438-140">INPUTS</span></span>

### <span data-ttu-id="a3438-141">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="a3438-141">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="a3438-142">System.String</span><span class="sxs-lookup"><span data-stu-id="a3438-142">System.String</span></span>

### <span data-ttu-id="a3438-143">System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.SettingNames, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="a3438-143">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.SettingNames, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="a3438-144">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a3438-144">OUTPUTS</span></span>

### <span data-ttu-id="a3438-145">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="a3438-145">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="a3438-146">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="a3438-146">NOTES</span></span>

## <span data-ttu-id="a3438-147">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="a3438-147">RELATED LINKS</span></span>

[<span data-ttu-id="a3438-148">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="a3438-148">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)

[<span data-ttu-id="a3438-149">Set-AzVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="a3438-149">Set-AzVMOperatingSystem</span></span>](./Set-AzVMOperatingSystem.md)

[<span data-ttu-id="a3438-150">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="a3438-150">New-AzVMConfig</span></span>](./New-AzVMConfig.md)
