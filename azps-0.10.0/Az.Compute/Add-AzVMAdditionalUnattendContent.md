---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 50B64FFE-8277-4DAA-805A-271123B35355
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmadditionalunattendcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Add-AzVMAdditionalUnattendContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Add-AzVMAdditionalUnattendContent.md
ms.openlocfilehash: e4359629da6f4df4c8da26e5ade2b2652c0762e4
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93840968"
---
# <span data-ttu-id="dee10-101">Add-AzVMAdditionalUnattendContent</span><span class="sxs-lookup"><span data-stu-id="dee10-101">Add-AzVMAdditionalUnattendContent</span></span>

## <span data-ttu-id="dee10-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="dee10-102">SYNOPSIS</span></span>
<span data-ttu-id="dee10-103">Fügt der Antwortdatei für das unbeaufsichtigte Windows Setup Informationen hinzu.</span><span class="sxs-lookup"><span data-stu-id="dee10-103">Adds information to the unattended Windows Setup answer file.</span></span>

## <span data-ttu-id="dee10-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="dee10-104">SYNTAX</span></span>

```
Add-AzVMAdditionalUnattendContent [-VM] <PSVirtualMachine> [[-Content] <String>]
 [[-SettingName] <SettingNames>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dee10-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dee10-105">DESCRIPTION</span></span>
<span data-ttu-id="dee10-106">Das Cmdlet **Add-AzVMAdditionalUnattendContent** fügt der Antwortdatei für das unbeaufsichtigte Windows Setup Informationen hinzu.</span><span class="sxs-lookup"><span data-stu-id="dee10-106">The **Add-AzVMAdditionalUnattendContent** cmdlet adds information to the unattended Windows Setup answer file.</span></span>
<span data-ttu-id="dee10-107">Geben Sie zusätzliche formatierte XML-Basis 64-codierte Informationen an, die dieses Cmdlet der unattend.xml-Datei hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="dee10-107">Specify additional base 64 encoded .xml formatted information that this cmdlet adds to the unattend.xml file.</span></span>

## <span data-ttu-id="dee10-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="dee10-108">EXAMPLES</span></span>

### <span data-ttu-id="dee10-109">Beispiel 1: Hinzufügen von Inhalten zu unattend.xml</span><span class="sxs-lookup"><span data-stu-id="dee10-109">Example 1: Add content to unattend.xml</span></span>
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id 
PS C:\> $Credential = Get-Credential
PS C:\> $VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine  -Windows -ComputerName "Contoso26" -Credential $Credential
PS C:\> $AucContent = "<UserAccounts><AdministratorPassword><Value>" + "Password" + "</Value><PlainText>true</PlainText></AdministratorPassword></UserAccounts>";
PS C:\> $VirtualMachine = Add-AzVMAdditionalUnattendContent -VM $VirtualMachine -Content $AucContent -SettingName "AutoLogon"
```

<span data-ttu-id="dee10-110">Der erste Befehl ruft den Verfügbarkeits Satz mit dem Namen AvailablitySet03 in der Ressourcengruppe mit dem Namen ResourceGroup11 ab und speichert dieses Objekt dann in der $AvailabilitySet Variablen.</span><span class="sxs-lookup"><span data-stu-id="dee10-110">The first command gets the availability set named AvailablitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>

<span data-ttu-id="dee10-111">Der zweite Befehl erstellt ein Objekt eines virtuellen Computers und speichert es dann in der $VirtualMachine-Variablen.</span><span class="sxs-lookup"><span data-stu-id="dee10-111">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="dee10-112">Der Befehl weist dem virtuellen Computer einen Namen und eine Größe zu.</span><span class="sxs-lookup"><span data-stu-id="dee10-112">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="dee10-113">Der virtuelle Computer gehört zum verfügbaren Verfügbarkeits Satz, der in $AvailabilitySet gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="dee10-113">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>

<span data-ttu-id="dee10-114">Der dritte Befehl erstellt ein Anmeldeinformationsobjekt mithilfe des Get-Credential-Cmdlets und speichert dann das Ergebnis in der $Credential-Variablen.</span><span class="sxs-lookup"><span data-stu-id="dee10-114">The third command creates a credential object by using the Get-Credential cmdlet, and then stores the result in the $Credential variable.</span></span>
<span data-ttu-id="dee10-115">Der Befehl fordert Sie auf, einen Benutzernamen und ein Kennwort einzugeben.</span><span class="sxs-lookup"><span data-stu-id="dee10-115">The command prompts you for a user name and password.</span></span>
<span data-ttu-id="dee10-116">Wenn Sie weitere Informationen wünschen, geben Sie `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="dee10-116">For more information, type `Get-Help Get-Credential`.</span></span>

<span data-ttu-id="dee10-117">Der vierte Befehl verwendet das Cmdlet " **Satz-AzVMOperatingSystem** ", um den in $VirtualMachine gespeicherten virtuellen Computer zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="dee10-117">The fourth command uses the **Set-AzVMOperatingSystem** cmdlet to configure the virtual machine stored in $VirtualMachine.</span></span>

<span data-ttu-id="dee10-118">Der fünfte Befehl weist Inhalt der $AucContent Variablen zu.</span><span class="sxs-lookup"><span data-stu-id="dee10-118">The fifth command assigns content to the $AucContent variable.</span></span>
<span data-ttu-id="dee10-119">Der Inhalt enthält ein Kennwort.</span><span class="sxs-lookup"><span data-stu-id="dee10-119">The content includes a password.</span></span>

<span data-ttu-id="dee10-120">Der endgültige Befehl fügt den in $AucContent gespeicherten Inhalt der unattend.xml Datei hinzu.</span><span class="sxs-lookup"><span data-stu-id="dee10-120">The final command adds the content stored in $AucContent to the unattend.xml file.</span></span>

## <span data-ttu-id="dee10-121">Parameter</span><span class="sxs-lookup"><span data-stu-id="dee10-121">PARAMETERS</span></span>

### <span data-ttu-id="dee10-122">– Inhalt</span><span class="sxs-lookup"><span data-stu-id="dee10-122">-Content</span></span>
<span data-ttu-id="dee10-123">Gibt den 64-codierten XML-formatierten Inhalt an.</span><span class="sxs-lookup"><span data-stu-id="dee10-123">Specifies base 64 encoded XML formatted content.</span></span>
<span data-ttu-id="dee10-124">Dieses Cmdlet fügt den Inhalt der unattend.xml-Datei hinzu.</span><span class="sxs-lookup"><span data-stu-id="dee10-124">This cmdlet adds the content to the unattend.xml file.</span></span>
<span data-ttu-id="dee10-125">Der XML-Inhalt muss kleiner als 4 KB sein und muss das Stammelement für die Einstellung oder das Feature enthalten, die von diesem Cmdlet eingefügt wird.</span><span class="sxs-lookup"><span data-stu-id="dee10-125">The XML content must be less than 4 KB and must include the root element for the setting or feature that this cmdlet inserts.</span></span>

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

### <span data-ttu-id="dee10-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dee10-126">-DefaultProfile</span></span>
<span data-ttu-id="dee10-127">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="dee10-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dee10-128">-SettingName</span><span class="sxs-lookup"><span data-stu-id="dee10-128">-SettingName</span></span>
<span data-ttu-id="dee10-129">Gibt den Namen der Einstellung an, auf die der Inhalt angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="dee10-129">Specifies the name of the setting to which the content applies.</span></span>
<span data-ttu-id="dee10-130">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="dee10-130">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="dee10-131">FirstLogonCommands</span><span class="sxs-lookup"><span data-stu-id="dee10-131">FirstLogonCommands</span></span>
- <span data-ttu-id="dee10-132">Autologon</span><span class="sxs-lookup"><span data-stu-id="dee10-132">AutoLogon</span></span>

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

### <span data-ttu-id="dee10-133">-VM</span><span class="sxs-lookup"><span data-stu-id="dee10-133">-VM</span></span>
<span data-ttu-id="dee10-134">Gibt das Objekt des virtuellen Computers an, das von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="dee10-134">Specifies the virtual machine object that this cmdlet modifies.</span></span>
<span data-ttu-id="dee10-135">Verwenden Sie das Cmdlet [Get-AzVM](./Get-AzVM.md) , um ein Objekt eines virtuellen Computers zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="dee10-135">To obtain a virtual machine object, use the [Get-AzVM](./Get-AzVM.md) cmdlet.</span></span>
<span data-ttu-id="dee10-136">Erstellen Sie ein Objekt eines virtuellen Computers mit dem Cmdlet [New-AzVMConfig](./New-AzVMConfig.md) .</span><span class="sxs-lookup"><span data-stu-id="dee10-136">Create a virtual machine object by using the [New-AzVMConfig](./New-AzVMConfig.md) cmdlet.</span></span>

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

### <span data-ttu-id="dee10-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dee10-137">CommonParameters</span></span>
<span data-ttu-id="dee10-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dee10-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dee10-139">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dee10-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dee10-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="dee10-140">INPUTS</span></span>

### <span data-ttu-id="dee10-141">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="dee10-141">PSVirtualMachine</span></span>
<span data-ttu-id="dee10-142">Der Parameter "VM" akzeptiert den Wert vom Typ "PSVirtualMachine" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="dee10-142">Parameter 'VM' accepts value of type 'PSVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="dee10-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="dee10-143">OUTPUTS</span></span>

### <span data-ttu-id="dee10-144">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="dee10-144">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="dee10-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="dee10-145">NOTES</span></span>

## <span data-ttu-id="dee10-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="dee10-146">RELATED LINKS</span></span>

[<span data-ttu-id="dee10-147">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="dee10-147">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)

[<span data-ttu-id="dee10-148">Satz-AzVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="dee10-148">Set-AzVMOperatingSystem</span></span>](./Set-AzVMOperatingSystem.md)

[<span data-ttu-id="dee10-149">Neu – AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="dee10-149">New-AzVMConfig</span></span>](./New-AzVMConfig.md)
