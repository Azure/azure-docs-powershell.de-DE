---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 50B64FFE-8277-4DAA-805A-271123B35355
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVMAdditionalUnattendContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVMAdditionalUnattendContent.md
ms.openlocfilehash: 0c823dd974fd2d01c7502c4cf45e67769e442526
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93483145"
---
# <span data-ttu-id="60748-101">Add-AzureRmVMAdditionalUnattendContent</span><span class="sxs-lookup"><span data-stu-id="60748-101">Add-AzureRmVMAdditionalUnattendContent</span></span>

## <span data-ttu-id="60748-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="60748-102">SYNOPSIS</span></span>
<span data-ttu-id="60748-103">Fügt der Antwortdatei für das unbeaufsichtigte Windows Setup Informationen hinzu.</span><span class="sxs-lookup"><span data-stu-id="60748-103">Adds information to the unattended Windows Setup answer file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="60748-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="60748-104">SYNTAX</span></span>

```
Add-AzureRmVMAdditionalUnattendContent [-VM] <PSVirtualMachine> [[-Content] <String>]
 [[-SettingName] <SettingNames>] [<CommonParameters>]
```

## <span data-ttu-id="60748-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="60748-105">DESCRIPTION</span></span>
<span data-ttu-id="60748-106">Das Cmdlet **Add-AzureRmVMAdditionalUnattendContent** fügt der Antwortdatei für das unbeaufsichtigte Windows Setup Informationen hinzu.</span><span class="sxs-lookup"><span data-stu-id="60748-106">The **Add-AzureRmVMAdditionalUnattendContent** cmdlet adds information to the unattended Windows Setup answer file.</span></span>
<span data-ttu-id="60748-107">Geben Sie zusätzliche formatierte XML-Basis 64-codierte Informationen an, die dieses Cmdlet der unattend.xml-Datei hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="60748-107">Specify additional base 64 encoded .xml formatted information that this cmdlet adds to the unattend.xml file.</span></span>

## <span data-ttu-id="60748-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="60748-108">EXAMPLES</span></span>

### <span data-ttu-id="60748-109">Beispiel 1: Hinzufügen von Inhalten zu unattend.xml</span><span class="sxs-lookup"><span data-stu-id="60748-109">Example 1: Add content to unattend.xml</span></span>
```
PS C:\> $AvailabilitySet = Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id 
PS C:\> $Credential = Get-Credential
PS C:\> $VirtualMachine = Set-AzureRmVMOperatingSystem -VM $VirtualMachine  -Windows -ComputerName "Contoso26" -Credential $Credential
PS C:\> $AucContent = "<UserAccounts><AdministratorPassword><Value>" + "Password" + "</Value><PlainText>true</PlainText></AdministratorPassword></UserAccounts>";
PS C:\> $VirtualMachine = Add-AzureRmVMAdditionalUnattendContent -VM $VirtualMachine -Content $AucContent -SettingName "AutoLogon"
```

<span data-ttu-id="60748-110">Der erste Befehl ruft den Verfügbarkeits Satz mit dem Namen AvailablitySet03 in der Ressourcengruppe mit dem Namen ResourceGroup11 ab und speichert dieses Objekt dann in der $AvailabilitySet Variablen.</span><span class="sxs-lookup"><span data-stu-id="60748-110">The first command gets the availability set named AvailablitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>

<span data-ttu-id="60748-111">Der zweite Befehl erstellt ein Objekt eines virtuellen Computers und speichert es dann in der $VirtualMachine-Variablen.</span><span class="sxs-lookup"><span data-stu-id="60748-111">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="60748-112">Der Befehl weist dem virtuellen Computer einen Namen und eine Größe zu.</span><span class="sxs-lookup"><span data-stu-id="60748-112">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="60748-113">Der virtuelle Computer gehört zum verfügbaren Verfügbarkeits Satz, der in $AvailabilitySet gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="60748-113">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>

<span data-ttu-id="60748-114">Der dritte Befehl erstellt ein Anmeldeinformationsobjekt mithilfe des Get-Credential-Cmdlets und speichert dann das Ergebnis in der $Credential-Variablen.</span><span class="sxs-lookup"><span data-stu-id="60748-114">The third command creates a credential object by using the Get-Credential cmdlet, and then stores the result in the $Credential variable.</span></span>
<span data-ttu-id="60748-115">Der Befehl fordert Sie auf, einen Benutzernamen und ein Kennwort einzugeben.</span><span class="sxs-lookup"><span data-stu-id="60748-115">The command prompts you for a user name and password.</span></span>
<span data-ttu-id="60748-116">Wenn Sie weitere Informationen wünschen, geben Sie `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="60748-116">For more information, type `Get-Help Get-Credential`.</span></span>

<span data-ttu-id="60748-117">Der vierte Befehl verwendet das Cmdlet " **Satz-AzureRmVMOperatingSystem** ", um den in $VirtualMachine gespeicherten virtuellen Computer zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="60748-117">The fourth command uses the **Set-AzureRmVMOperatingSystem** cmdlet to configure the virtual machine stored in $VirtualMachine.</span></span>

<span data-ttu-id="60748-118">Der fünfte Befehl weist Inhalt der $AucContent Variablen zu.</span><span class="sxs-lookup"><span data-stu-id="60748-118">The fifth command assigns content to the $AucContent variable.</span></span>
<span data-ttu-id="60748-119">Der Inhalt enthält ein Kennwort.</span><span class="sxs-lookup"><span data-stu-id="60748-119">The content includes a password.</span></span>

<span data-ttu-id="60748-120">Der endgültige Befehl fügt den in $AucContent gespeicherten Inhalt der unattend.xml Datei hinzu.</span><span class="sxs-lookup"><span data-stu-id="60748-120">The final command adds the content stored in $AucContent to the unattend.xml file.</span></span>

## <span data-ttu-id="60748-121">Parameter</span><span class="sxs-lookup"><span data-stu-id="60748-121">PARAMETERS</span></span>

### <span data-ttu-id="60748-122">– Inhalt</span><span class="sxs-lookup"><span data-stu-id="60748-122">-Content</span></span>
<span data-ttu-id="60748-123">Gibt den 64-codierten XML-formatierten Inhalt an.</span><span class="sxs-lookup"><span data-stu-id="60748-123">Specifies base 64 encoded XML formatted content.</span></span>
<span data-ttu-id="60748-124">Dieses Cmdlet fügt den Inhalt der unattend.xml-Datei hinzu.</span><span class="sxs-lookup"><span data-stu-id="60748-124">This cmdlet adds the content to the unattend.xml file.</span></span>
<span data-ttu-id="60748-125">Der XML-Inhalt muss kleiner als 4 KB sein und muss das Stammelement für die Einstellung oder das Feature enthalten, die von diesem Cmdlet eingefügt wird.</span><span class="sxs-lookup"><span data-stu-id="60748-125">The XML content must be less than 4 KB and must include the root element for the setting or feature that this cmdlet inserts.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60748-126">-SettingName</span><span class="sxs-lookup"><span data-stu-id="60748-126">-SettingName</span></span>
<span data-ttu-id="60748-127">Gibt den Namen der Einstellung an, auf die der Inhalt angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="60748-127">Specifies the name of the setting to which the content applies.</span></span>
<span data-ttu-id="60748-128">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="60748-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="60748-129">FirstLogonCommands</span><span class="sxs-lookup"><span data-stu-id="60748-129">FirstLogonCommands</span></span>
- <span data-ttu-id="60748-130">Autologon</span><span class="sxs-lookup"><span data-stu-id="60748-130">AutoLogon</span></span>

```yaml
Type: SettingNames
Parameter Sets: (All)
Aliases: 
Accepted values: AutoLogon, FirstLogonCommands

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60748-131">-VM</span><span class="sxs-lookup"><span data-stu-id="60748-131">-VM</span></span>
<span data-ttu-id="60748-132">Gibt das Objekt des virtuellen Computers an, das von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="60748-132">Specifies the virtual machine object that this cmdlet modifies.</span></span>
<span data-ttu-id="60748-133">Verwenden Sie das Cmdlet [Get-AzureRmVM](./Get-AzureRmVM.md) , um ein Objekt eines virtuellen Computers zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="60748-133">To obtain a virtual machine object, use the [Get-AzureRmVM](./Get-AzureRmVM.md) cmdlet.</span></span>
<span data-ttu-id="60748-134">Erstellen Sie ein Objekt eines virtuellen Computers mit dem Cmdlet [New-AzureRmVMConfig](./New-AzureRmVMConfig.md) .</span><span class="sxs-lookup"><span data-stu-id="60748-134">Create a virtual machine object by using the [New-AzureRmVMConfig](./New-AzureRmVMConfig.md) cmdlet.</span></span>

```yaml
Type: PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="60748-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60748-135">CommonParameters</span></span>
<span data-ttu-id="60748-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60748-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60748-137">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="60748-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60748-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="60748-138">INPUTS</span></span>

### <span data-ttu-id="60748-139">Keine</span><span class="sxs-lookup"><span data-stu-id="60748-139">None</span></span>
<span data-ttu-id="60748-140">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="60748-140">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="60748-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="60748-141">OUTPUTS</span></span>

## <span data-ttu-id="60748-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="60748-142">NOTES</span></span>

## <span data-ttu-id="60748-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="60748-143">RELATED LINKS</span></span>

[<span data-ttu-id="60748-144">Get-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="60748-144">Get-AzureRmAvailabilitySet</span></span>](./Get-AzureRmAvailabilitySet.md)

[<span data-ttu-id="60748-145">Satz-AzureRmVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="60748-145">Set-AzureRmVMOperatingSystem</span></span>](./Set-AzureRmVMOperatingSystem.md)

[<span data-ttu-id="60748-146">Neu – AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="60748-146">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)
