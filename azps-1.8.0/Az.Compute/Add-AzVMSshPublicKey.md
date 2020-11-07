---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 3CE367B1-7685-4046-8E9C-CE680B5AE03F
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmsshpublickey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMSshPublicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMSshPublicKey.md
ms.openlocfilehash: 432de351ae62650ff4e4e2efae0550fab2fa6091
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93661585"
---
# <span data-ttu-id="1169c-101">Add-AzVMSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="1169c-101">Add-AzVMSshPublicKey</span></span>

## <span data-ttu-id="1169c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1169c-102">SYNOPSIS</span></span>
<span data-ttu-id="1169c-103">Fügt die öffentlichen Schlüssel für SSH für einen virtuellen Computer hinzu.</span><span class="sxs-lookup"><span data-stu-id="1169c-103">Adds the public keys for SSH for a virtual machine.</span></span>

## <span data-ttu-id="1169c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1169c-104">SYNTAX</span></span>

```
Add-AzVMSshPublicKey [-VM] <PSVirtualMachine> [[-KeyData] <String>] [[-Path] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1169c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1169c-105">DESCRIPTION</span></span>
<span data-ttu-id="1169c-106">Das Cmdlet **Add-AzVMSshPublicKey** fügt die öffentlichen Schlüssel hinzu, die Sie zum Herstellen einer Verbindung mit einem virtuellen Computer über Secure Shell (SSH) verwenden können.</span><span class="sxs-lookup"><span data-stu-id="1169c-106">The **Add-AzVMSshPublicKey** cmdlet adds the public keys that you can use to connect to a virtual machine over Secure Shell (SSH).</span></span>

## <span data-ttu-id="1169c-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1169c-107">EXAMPLES</span></span>

### <span data-ttu-id="1169c-108">Beispiel 1: Hinzufügen eines öffentlichen Schlüssels zu einem virtuellen Computer</span><span class="sxs-lookup"><span data-stu-id="1169c-108">Example 1: Add a public key to a virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
PS C:\> $VirtualMachine = Add-AzVMSshPublicKey -VM $VirtualMachine -KeyData "MIIDszCCApugAwIBAgIJALBV9YJCF/tAMA0GCSq12Ib3DQEB21QUAMEUxCzAJBgNV" -Path "/home/admin/.ssh/authorized_keys"
```

<span data-ttu-id="1169c-109">Der erste Befehl ruft den virtuellen Computer mit dem Namen VirtualMachine07 mit dem Cmdlet **Get-AzVM** ab.</span><span class="sxs-lookup"><span data-stu-id="1169c-109">The first command gets the virtual machine named VirtualMachine07 by using the **Get-AzVM** cmdlet.</span></span>
<span data-ttu-id="1169c-110">Der Befehl speichert den virtuellen Computer in der $VirtualMachine-Variablen.</span><span class="sxs-lookup"><span data-stu-id="1169c-110">The command stores the virtual machine in the $VirtualMachine variable.</span></span>
<span data-ttu-id="1169c-111">Mit dem zweiten Befehl wird der öffentliche Schlüssel an der Position auf VirtualMachine07 hinzugefügt, die vom path-Parameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="1169c-111">The second command adds the public key to the location on VirtualMachine07 that the Path parameter specifies.</span></span>

## <span data-ttu-id="1169c-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="1169c-112">PARAMETERS</span></span>

### <span data-ttu-id="1169c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1169c-113">-DefaultProfile</span></span>
<span data-ttu-id="1169c-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1169c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1169c-115">-KeyData</span><span class="sxs-lookup"><span data-stu-id="1169c-115">-KeyData</span></span>
<span data-ttu-id="1169c-116">Gibt eine Basis 64-Codierung eines öffentlichen Schlüssels an.</span><span class="sxs-lookup"><span data-stu-id="1169c-116">Specifies a base 64 encoding of a public key.</span></span>
<span data-ttu-id="1169c-117">Sie können mithilfe von ssh eine Verbindung mit einem virtuellen Computer herstellen oder mithilfe des Schlüssels, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="1169c-117">You can connect to a virtual machine by using SSH or by using the key that this parameter specifies.</span></span>

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

### <span data-ttu-id="1169c-118">-Path</span><span class="sxs-lookup"><span data-stu-id="1169c-118">-Path</span></span>
<span data-ttu-id="1169c-119">Gibt den vollständigen Pfad einer Datei auf dem virtuellen Computer an, in dem dieses Cmdlet den öffentlichen SSH-Schlüssel speichert.</span><span class="sxs-lookup"><span data-stu-id="1169c-119">Specifies the full path of a file, on the virtual machine, where this cmdlet stores the SSH public key.</span></span>
<span data-ttu-id="1169c-120">Wenn die Datei bereits vorhanden ist, hängt dieses Cmdlet den Schlüssel an die Datei an.</span><span class="sxs-lookup"><span data-stu-id="1169c-120">If the file already exists, this cmdlet appends the key to the file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1169c-121">-VM</span><span class="sxs-lookup"><span data-stu-id="1169c-121">-VM</span></span>
<span data-ttu-id="1169c-122">Gibt das Objekt des virtuellen Computers an, das von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="1169c-122">Specifies the virtual machine object that this cmdlet modifies.</span></span>
<span data-ttu-id="1169c-123">Verwenden Sie das Cmdlet [Get-AzVM](./Get-AzVM.md) , um ein Objekt eines virtuellen Computers zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="1169c-123">To obtain a virtual machine object, use the [Get-AzVM](./Get-AzVM.md) cmdlet.</span></span>
<span data-ttu-id="1169c-124">Sie können das Cmdlet [New-AzVMConfig](./New-AzVMConfig.md) verwenden, um ein Objekt eines virtuellen Computers zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="1169c-124">You can use the [New-AzVMConfig](./New-AzVMConfig.md) cmdlet to create a virtual machine object.</span></span>

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

### <span data-ttu-id="1169c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1169c-125">CommonParameters</span></span>
<span data-ttu-id="1169c-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1169c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1169c-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1169c-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1169c-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1169c-128">INPUTS</span></span>

### <span data-ttu-id="1169c-129">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="1169c-129">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="1169c-130">System. String</span><span class="sxs-lookup"><span data-stu-id="1169c-130">System.String</span></span>

## <span data-ttu-id="1169c-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1169c-131">OUTPUTS</span></span>

### <span data-ttu-id="1169c-132">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="1169c-132">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="1169c-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="1169c-133">NOTES</span></span>

## <span data-ttu-id="1169c-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1169c-134">RELATED LINKS</span></span>

[<span data-ttu-id="1169c-135">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="1169c-135">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="1169c-136">Neu – AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="1169c-136">New-AzVMConfig</span></span>](./New-AzVMConfig.md)
