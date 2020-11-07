---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 3CE367B1-7685-4046-8E9C-CE680B5AE03F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVMSshPublicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVMSshPublicKey.md
ms.openlocfilehash: b4cbc3ba7dd90d2810c4833fe1b74c13541fcb7a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662593"
---
# <span data-ttu-id="ef805-101">Add-AzureRmVMSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="ef805-101">Add-AzureRmVMSshPublicKey</span></span>

## <span data-ttu-id="ef805-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ef805-102">SYNOPSIS</span></span>
<span data-ttu-id="ef805-103">Fügt die öffentlichen Schlüssel für SSH für einen virtuellen Computer hinzu.</span><span class="sxs-lookup"><span data-stu-id="ef805-103">Adds the public keys for SSH for a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ef805-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ef805-104">SYNTAX</span></span>

```
Add-AzureRmVMSshPublicKey [-VM] <PSVirtualMachine> [[-KeyData] <String>] [[-Path] <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="ef805-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ef805-105">DESCRIPTION</span></span>
<span data-ttu-id="ef805-106">Das Cmdlet **Add-AzureRmVMSshPublicKey** fügt die öffentlichen Schlüssel hinzu, die Sie zum Herstellen einer Verbindung mit einem virtuellen Computer über Secure Shell (SSH) verwenden können.</span><span class="sxs-lookup"><span data-stu-id="ef805-106">The **Add-AzureRmVMSshPublicKey** cmdlet adds the public keys that you can use to connect to a virtual machine over Secure Shell (SSH).</span></span>

## <span data-ttu-id="ef805-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ef805-107">EXAMPLES</span></span>

### <span data-ttu-id="ef805-108">Beispiel 1: Hinzufügen eines öffentlichen Schlüssels zu einem virtuellen Computer</span><span class="sxs-lookup"><span data-stu-id="ef805-108">Example 1: Add a public key to a virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
PS C:\> $VirtualMachine = Add-AzureRmVMSshPublicKey -VM $VirtualMachine -KeyData "MIIDszCCApugAwIBAgIJALBV9YJCF/tAMA0GCSq12Ib3DQEB21QUAMEUxCzAJBgNV" -Path "/home/admin/.ssh/authorized_keys"
```

<span data-ttu-id="ef805-109">Der erste Befehl ruft den virtuellen Computer mit dem Namen VirtualMachine07 mit dem Cmdlet **Get-AzureRmVM** ab.</span><span class="sxs-lookup"><span data-stu-id="ef805-109">The first command gets the virtual machine named VirtualMachine07 by using the **Get-AzureRmVM** cmdlet.</span></span>
<span data-ttu-id="ef805-110">Der Befehl speichert den virtuellen Computer in der $VirtualMachine-Variablen.</span><span class="sxs-lookup"><span data-stu-id="ef805-110">The command stores the virtual machine in the $VirtualMachine variable.</span></span>

<span data-ttu-id="ef805-111">Mit dem zweiten Befehl wird der öffentliche Schlüssel an der Position auf VirtualMachine07 hinzugefügt, die vom path-Parameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="ef805-111">The second command adds the public key to the location on VirtualMachine07 that the Path parameter specifies.</span></span>

## <span data-ttu-id="ef805-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="ef805-112">PARAMETERS</span></span>

### <span data-ttu-id="ef805-113">-KeyData</span><span class="sxs-lookup"><span data-stu-id="ef805-113">-KeyData</span></span>
<span data-ttu-id="ef805-114">Gibt eine Basis 64-Codierung eines öffentlichen Schlüssels an.</span><span class="sxs-lookup"><span data-stu-id="ef805-114">Specifies a base 64 encoding of a public key.</span></span>
<span data-ttu-id="ef805-115">Sie können mithilfe von ssh eine Verbindung mit einem virtuellen Computer herstellen oder mithilfe des Schlüssels, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="ef805-115">You can connect to a virtual machine by using SSH or by using the key that this parameter specifies.</span></span>

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

### <span data-ttu-id="ef805-116">-Path</span><span class="sxs-lookup"><span data-stu-id="ef805-116">-Path</span></span>
<span data-ttu-id="ef805-117">Gibt den vollständigen Pfad einer Datei auf dem virtuellen Computer an, in dem dieses Cmdlet den öffentlichen SSH-Schlüssel speichert.</span><span class="sxs-lookup"><span data-stu-id="ef805-117">Specifies the full path of a file, on the virtual machine, where this cmdlet stores the SSH public key.</span></span>
<span data-ttu-id="ef805-118">Wenn die Datei bereits vorhanden ist, hängt dieses Cmdlet den Schlüssel an die Datei an.</span><span class="sxs-lookup"><span data-stu-id="ef805-118">If the file already exists, this cmdlet appends the key to the file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef805-119">-VM</span><span class="sxs-lookup"><span data-stu-id="ef805-119">-VM</span></span>
<span data-ttu-id="ef805-120">Gibt das Objekt des virtuellen Computers an, das von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="ef805-120">Specifies the virtual machine object that this cmdlet modifies.</span></span>
<span data-ttu-id="ef805-121">Verwenden Sie das Cmdlet [Get-AzureRmVM](./Get-AzureRmVM.md) , um ein Objekt eines virtuellen Computers zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="ef805-121">To obtain a virtual machine object, use the [Get-AzureRmVM](./Get-AzureRmVM.md) cmdlet.</span></span>
<span data-ttu-id="ef805-122">Sie können das Cmdlet [New-AzureRmVMConfig](./New-AzureRmVMConfig.md) verwenden, um ein Objekt eines virtuellen Computers zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="ef805-122">You can use the [New-AzureRmVMConfig](./New-AzureRmVMConfig.md) cmdlet to create a virtual machine object.</span></span>

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

### <span data-ttu-id="ef805-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef805-123">CommonParameters</span></span>
<span data-ttu-id="ef805-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef805-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef805-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef805-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef805-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ef805-126">INPUTS</span></span>

### <span data-ttu-id="ef805-127">Keine</span><span class="sxs-lookup"><span data-stu-id="ef805-127">None</span></span>
<span data-ttu-id="ef805-128">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="ef805-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ef805-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ef805-129">OUTPUTS</span></span>

## <span data-ttu-id="ef805-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="ef805-130">NOTES</span></span>

## <span data-ttu-id="ef805-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ef805-131">RELATED LINKS</span></span>

[<span data-ttu-id="ef805-132">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="ef805-132">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="ef805-133">Neu – AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="ef805-133">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)
