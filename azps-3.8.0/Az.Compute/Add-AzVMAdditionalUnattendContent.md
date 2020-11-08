---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 50B64FFE-8277-4DAA-805A-271123B35355
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmadditionalunattendcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMAdditionalUnattendContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMAdditionalUnattendContent.md
ms.openlocfilehash: 05f100e730cb808bf40bbec60386901eb39020ce
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93994998"
---
# <span data-ttu-id="1fc72-101">Add-AzVMAdditionalUnattendContent</span><span class="sxs-lookup"><span data-stu-id="1fc72-101">Add-AzVMAdditionalUnattendContent</span></span>

## <span data-ttu-id="1fc72-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1fc72-102">SYNOPSIS</span></span>
<span data-ttu-id="1fc72-103">Fügt der Antwortdatei für das unbeaufsichtigte Windows Setup Informationen hinzu.</span><span class="sxs-lookup"><span data-stu-id="1fc72-103">Adds information to the unattended Windows Setup answer file.</span></span>

## <span data-ttu-id="1fc72-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1fc72-104">SYNTAX</span></span>

```
Add-AzVMAdditionalUnattendContent [-VM] <PSVirtualMachine> [[-Content] <String>]
 [[-SettingName] <SettingNames>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1fc72-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1fc72-105">DESCRIPTION</span></span>
<span data-ttu-id="1fc72-106">Das Cmdlet **Add-AzVMAdditionalUnattendContent** fügt der Antwortdatei für das unbeaufsichtigte Windows Setup Informationen hinzu.</span><span class="sxs-lookup"><span data-stu-id="1fc72-106">The **Add-AzVMAdditionalUnattendContent** cmdlet adds information to the unattended Windows Setup answer file.</span></span>
<span data-ttu-id="1fc72-107">Geben Sie zusätzliche formatierte XML-Basis 64-codierte Informationen an, die dieses Cmdlet der unattend.xml-Datei hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="1fc72-107">Specify additional base 64 encoded .xml formatted information that this cmdlet adds to the unattend.xml file.</span></span>

## <span data-ttu-id="1fc72-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1fc72-108">EXAMPLES</span></span>

### <span data-ttu-id="1fc72-109">Beispiel 1: Hinzufügen von Inhalten zu unattend.xml</span><span class="sxs-lookup"><span data-stu-id="1fc72-109">Example 1: Add content to unattend.xml</span></span>
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id 
PS C:\> $Credential = Get-Credential
PS C:\> $VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine  -Windows -ComputerName "Contoso26" -Credential $Credential
PS C:\> $AucContent = "<UserAccounts><AdministratorPassword><Value>" + "Password" + "</Value><PlainText>true</PlainText></AdministratorPassword></UserAccounts>";
PS C:\> $VirtualMachine = Add-AzVMAdditionalUnattendContent -VM $VirtualMachine -Content $AucContent -SettingName "AutoLogon"
```

<span data-ttu-id="1fc72-110">Der erste Befehl ruft den Verfügbarkeits Satz mit dem Namen AvailabilitySet03 in der Ressourcengruppe mit dem Namen ResourceGroup11 ab und speichert dieses Objekt dann in der $AvailabilitySet Variablen.</span><span class="sxs-lookup"><span data-stu-id="1fc72-110">The first command gets the availability set named AvailabilitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="1fc72-111">Der zweite Befehl erstellt ein Objekt eines virtuellen Computers und speichert es dann in der $VirtualMachine-Variablen.</span><span class="sxs-lookup"><span data-stu-id="1fc72-111">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="1fc72-112">Der Befehl weist dem virtuellen Computer einen Namen und eine Größe zu.</span><span class="sxs-lookup"><span data-stu-id="1fc72-112">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="1fc72-113">Der virtuelle Computer gehört zum verfügbaren Verfügbarkeits Satz, der in $AvailabilitySet gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="1fc72-113">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="1fc72-114">Der dritte Befehl erstellt ein Anmeldeinformationsobjekt mithilfe des Get-Credential-Cmdlets und speichert dann das Ergebnis in der $Credential-Variablen.</span><span class="sxs-lookup"><span data-stu-id="1fc72-114">The third command creates a credential object by using the Get-Credential cmdlet, and then stores the result in the $Credential variable.</span></span>
<span data-ttu-id="1fc72-115">Der Befehl fordert Sie auf, einen Benutzernamen und ein Kennwort einzugeben.</span><span class="sxs-lookup"><span data-stu-id="1fc72-115">The command prompts you for a user name and password.</span></span>
<span data-ttu-id="1fc72-116">Wenn Sie weitere Informationen wünschen, geben Sie `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="1fc72-116">For more information, type `Get-Help Get-Credential`.</span></span>
<span data-ttu-id="1fc72-117">Der vierte Befehl verwendet das Cmdlet " **Satz-AzVMOperatingSystem** ", um den in $VirtualMachine gespeicherten virtuellen Computer zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="1fc72-117">The fourth command uses the **Set-AzVMOperatingSystem** cmdlet to configure the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="1fc72-118">Der fünfte Befehl weist Inhalt der $AucContent Variablen zu.</span><span class="sxs-lookup"><span data-stu-id="1fc72-118">The fifth command assigns content to the $AucContent variable.</span></span>
<span data-ttu-id="1fc72-119">Der Inhalt enthält ein Kennwort.</span><span class="sxs-lookup"><span data-stu-id="1fc72-119">The content includes a password.</span></span>
<span data-ttu-id="1fc72-120">Der endgültige Befehl fügt den in $AucContent gespeicherten Inhalt der unattend.xml Datei hinzu.</span><span class="sxs-lookup"><span data-stu-id="1fc72-120">The final command adds the content stored in $AucContent to the unattend.xml file.</span></span>

## <span data-ttu-id="1fc72-121">Parameter</span><span class="sxs-lookup"><span data-stu-id="1fc72-121">PARAMETERS</span></span>

### <span data-ttu-id="1fc72-122">– Inhalt</span><span class="sxs-lookup"><span data-stu-id="1fc72-122">-Content</span></span>
<span data-ttu-id="1fc72-123">Gibt den 64-codierten XML-formatierten Inhalt an.</span><span class="sxs-lookup"><span data-stu-id="1fc72-123">Specifies base 64 encoded XML formatted content.</span></span>
<span data-ttu-id="1fc72-124">Dieses Cmdlet fügt den Inhalt der unattend.xml-Datei hinzu.</span><span class="sxs-lookup"><span data-stu-id="1fc72-124">This cmdlet adds the content to the unattend.xml file.</span></span>
<span data-ttu-id="1fc72-125">Der XML-Inhalt muss kleiner als 4 KB sein und muss das Stammelement für die Einstellung oder das Feature enthalten, die von diesem Cmdlet eingefügt wird.</span><span class="sxs-lookup"><span data-stu-id="1fc72-125">The XML content must be less than 4 KB and must include the root element for the setting or feature that this cmdlet inserts.</span></span>

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

### <span data-ttu-id="1fc72-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1fc72-126">-DefaultProfile</span></span>
<span data-ttu-id="1fc72-127">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1fc72-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1fc72-128">-SettingName</span><span class="sxs-lookup"><span data-stu-id="1fc72-128">-SettingName</span></span>
<span data-ttu-id="1fc72-129">Gibt den Namen der Einstellung an, auf die der Inhalt angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="1fc72-129">Specifies the name of the setting to which the content applies.</span></span>
<span data-ttu-id="1fc72-130">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="1fc72-130">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="1fc72-131">FirstLogonCommands</span><span class="sxs-lookup"><span data-stu-id="1fc72-131">FirstLogonCommands</span></span>
- <span data-ttu-id="1fc72-132">Autologon</span><span class="sxs-lookup"><span data-stu-id="1fc72-132">AutoLogon</span></span>

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

### <span data-ttu-id="1fc72-133">-VM</span><span class="sxs-lookup"><span data-stu-id="1fc72-133">-VM</span></span>
<span data-ttu-id="1fc72-134">Gibt das Objekt des virtuellen Computers an, das von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="1fc72-134">Specifies the virtual machine object that this cmdlet modifies.</span></span>
<span data-ttu-id="1fc72-135">Verwenden Sie das Cmdlet [Get-AzVM](./Get-AzVM.md) , um ein Objekt eines virtuellen Computers zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="1fc72-135">To obtain a virtual machine object, use the [Get-AzVM](./Get-AzVM.md) cmdlet.</span></span>
<span data-ttu-id="1fc72-136">Erstellen Sie ein Objekt eines virtuellen Computers mit dem Cmdlet [New-AzVMConfig](./New-AzVMConfig.md) .</span><span class="sxs-lookup"><span data-stu-id="1fc72-136">Create a virtual machine object by using the [New-AzVMConfig](./New-AzVMConfig.md) cmdlet.</span></span>

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

### <span data-ttu-id="1fc72-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1fc72-137">CommonParameters</span></span>
<span data-ttu-id="1fc72-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1fc72-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1fc72-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1fc72-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1fc72-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1fc72-140">INPUTS</span></span>

### <span data-ttu-id="1fc72-141">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="1fc72-141">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="1fc72-142">System. String</span><span class="sxs-lookup"><span data-stu-id="1fc72-142">System.String</span></span>

### <span data-ttu-id="1fc72-143">System. Nullable ' 1 [[Microsoft. Azure. Management. Compute. Models. SettingNames, Microsoft. Azure. Management. COMPUTE, Version = 23.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="1fc72-143">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.SettingNames, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="1fc72-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1fc72-144">OUTPUTS</span></span>

### <span data-ttu-id="1fc72-145">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="1fc72-145">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="1fc72-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="1fc72-146">NOTES</span></span>

## <span data-ttu-id="1fc72-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1fc72-147">RELATED LINKS</span></span>

[<span data-ttu-id="1fc72-148">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="1fc72-148">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)

[<span data-ttu-id="1fc72-149">Satz-AzVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="1fc72-149">Set-AzVMOperatingSystem</span></span>](./Set-AzVMOperatingSystem.md)

[<span data-ttu-id="1fc72-150">Neu – AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="1fc72-150">New-AzVMConfig</span></span>](./New-AzVMConfig.md)
