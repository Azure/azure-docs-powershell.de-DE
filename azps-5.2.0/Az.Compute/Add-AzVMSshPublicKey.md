---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 3CE367B1-7685-4046-8E9C-CE680B5AE03F
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmsshpublickey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMSshPublicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMSshPublicKey.md
ms.openlocfilehash: e17b495147c308d20d6d5b950914d26ce56a5706
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98305840"
---
# <span data-ttu-id="47cf2-101">Add-AzVMSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="47cf2-101">Add-AzVMSshPublicKey</span></span>

## <span data-ttu-id="47cf2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="47cf2-102">SYNOPSIS</span></span>
<span data-ttu-id="47cf2-103">Fügt die öffentlichen Schlüssel für SSH für einen virtuellen Computer hinzu, wenn nur die VM erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="47cf2-103">Adds the public keys for SSH for a virtual machine, when only creating the VM.</span></span>

## <span data-ttu-id="47cf2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="47cf2-104">SYNTAX</span></span>

```
Add-AzVMSshPublicKey [-VM] <PSVirtualMachine> [[-KeyData] <String>] [[-Path] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="47cf2-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="47cf2-105">DESCRIPTION</span></span>
<span data-ttu-id="47cf2-106">Das **Cmdlet "Add-AzVMSshPublicKey"** fügt die öffentlichen Schlüssel hinzu, die Sie verwenden können, um über SSH (Secure Shell) eine Verbindung mit einem virtuellen Linux-Computer herzustellen.</span><span class="sxs-lookup"><span data-stu-id="47cf2-106">The **Add-AzVMSshPublicKey** cmdlet adds the public keys that you can use to connect to a Linux virtual machine over Secure Shell (SSH).</span></span> <span data-ttu-id="47cf2-107">Dies kann nach der Erstellung von VM nicht verwendet werden. Wenn Sie versuchen, dies nach der Erstellung der VM ohne Update-AzVM zu verwenden, tritt kein Fehler auf. Wenn Sie den Befehl mit Update-AzVM verwenden, tritt ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="47cf2-107">This cannot be used after VM creation, if you try to use this after VM creation without Update-AzVM, there will be no error, if you use the command with Update-AzVM, the command will error.</span></span>

## <span data-ttu-id="47cf2-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="47cf2-108">EXAMPLES</span></span>

### <span data-ttu-id="47cf2-109">Beispiel 1: Hinzufügen eines öffentlichen Schlüssels zu einem virtuellen Computer</span><span class="sxs-lookup"><span data-stu-id="47cf2-109">Example 1: Add a public key to a virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
PS C:\> $VirtualMachine = Add-AzVMSshPublicKey -VM $VirtualMachine -KeyData "MIIDszCCApugAwIBAgIJALBV9YJCF/tAMA0GCSq12Ib3DQEB21QUAMEUxCzAJBgNV" -Path "/home/admin/.ssh/authorized_keys"
```

<span data-ttu-id="47cf2-110">Der erste Befehl ruft den virtuellen Computer "VirtualMachine07" mithilfe des **Get-AzVM-Cmdlets** ab.</span><span class="sxs-lookup"><span data-stu-id="47cf2-110">The first command gets the virtual machine named VirtualMachine07 by using the **Get-AzVM** cmdlet.</span></span>
<span data-ttu-id="47cf2-111">Der Befehl speichert den virtuellen Computer in der $VirtualMachine Variable.</span><span class="sxs-lookup"><span data-stu-id="47cf2-111">The command stores the virtual machine in the $VirtualMachine variable.</span></span>
<span data-ttu-id="47cf2-112">Der zweite Befehl fügt den öffentlichen Schlüssel dem vom Parameter "Path" angegebenen Speicherort in VirtualMachine07 hinzu.</span><span class="sxs-lookup"><span data-stu-id="47cf2-112">The second command adds the public key to the location on VirtualMachine07 that the Path parameter specifies.</span></span>

## <span data-ttu-id="47cf2-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="47cf2-113">PARAMETERS</span></span>

### <span data-ttu-id="47cf2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47cf2-114">-DefaultProfile</span></span>
<span data-ttu-id="47cf2-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="47cf2-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="47cf2-116">-KeyData</span><span class="sxs-lookup"><span data-stu-id="47cf2-116">-KeyData</span></span>
<span data-ttu-id="47cf2-117">Gibt die Basis-64-Codierung eines öffentlichen Schlüssels an.</span><span class="sxs-lookup"><span data-stu-id="47cf2-117">Specifies a base 64 encoding of a public key.</span></span>
<span data-ttu-id="47cf2-118">Sie können eine Verbindung mit einem virtuellen Linux-Computer herstellen, indem Sie SSH oder den schlüssel, den dieser Parameter angibt, verwenden.</span><span class="sxs-lookup"><span data-stu-id="47cf2-118">You can connect to a Linux virtual machine by using SSH or by using the key that this parameter specifies.</span></span>

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

### <span data-ttu-id="47cf2-119">-Path</span><span class="sxs-lookup"><span data-stu-id="47cf2-119">-Path</span></span>
<span data-ttu-id="47cf2-120">Gibt den vollständigen Pfad einer Datei auf dem virtuellen Computer an, auf dem dieses Cmdlet den öffentlichen SSH-Schlüssel speichert.</span><span class="sxs-lookup"><span data-stu-id="47cf2-120">Specifies the full path of a file, on the virtual machine, where this cmdlet stores the SSH public key.</span></span>
<span data-ttu-id="47cf2-121">Wenn die Datei bereits vorhanden ist, fügt dieses Cmdlet den Schlüssel an die Datei an.</span><span class="sxs-lookup"><span data-stu-id="47cf2-121">If the file already exists, this cmdlet appends the key to the file.</span></span>

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

### <span data-ttu-id="47cf2-122">-VM</span><span class="sxs-lookup"><span data-stu-id="47cf2-122">-VM</span></span>
<span data-ttu-id="47cf2-123">Gibt das Objekt des virtuellen Computers an, das von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="47cf2-123">Specifies the virtual machine object that this cmdlet modifies.</span></span>
<span data-ttu-id="47cf2-124">Verwenden Sie das [Get-AzVM-Cmdlet,](./Get-AzVM.md) um ein Objekt des virtuellen Computers zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="47cf2-124">To obtain a virtual machine object, use the [Get-AzVM](./Get-AzVM.md) cmdlet.</span></span>
<span data-ttu-id="47cf2-125">Sie können das [Cmdlet "New-AzVMConfig"](./New-AzVMConfig.md) verwenden, um ein Objekt für einen virtuellen Computer zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="47cf2-125">You can use the [New-AzVMConfig](./New-AzVMConfig.md) cmdlet to create a virtual machine object.</span></span>

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

### <span data-ttu-id="47cf2-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47cf2-126">CommonParameters</span></span>
<span data-ttu-id="47cf2-127">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47cf2-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47cf2-128">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="47cf2-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47cf2-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="47cf2-129">INPUTS</span></span>

### <span data-ttu-id="47cf2-130">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="47cf2-130">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="47cf2-131">System.String</span><span class="sxs-lookup"><span data-stu-id="47cf2-131">System.String</span></span>

## <span data-ttu-id="47cf2-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="47cf2-132">OUTPUTS</span></span>

### <span data-ttu-id="47cf2-133">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="47cf2-133">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="47cf2-134">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="47cf2-134">NOTES</span></span>

## <span data-ttu-id="47cf2-135">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="47cf2-135">RELATED LINKS</span></span>

[<span data-ttu-id="47cf2-136">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="47cf2-136">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="47cf2-137">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="47cf2-137">New-AzVMConfig</span></span>](./New-AzVMConfig.md)
