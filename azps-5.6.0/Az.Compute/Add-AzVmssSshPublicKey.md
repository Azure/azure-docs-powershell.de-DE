---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 9C216103-EB77-468E-8684-F5E5400B73A7
online version: https://docs.microsoft.com/powershell/module/az.compute/add-azvmsssshpublickey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssSshPublicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssSshPublicKey.md
ms.openlocfilehash: 17235c8790928b81b6d796d1d5d7b661c560be7c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101938896"
---
# <span data-ttu-id="8d252-101">Add-AzVmssSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="8d252-101">Add-AzVmssSshPublicKey</span></span>

## <span data-ttu-id="8d252-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8d252-102">SYNOPSIS</span></span>
<span data-ttu-id="8d252-103">Fügt dem VMSS öffentliche SSH-Schlüssel hinzu.</span><span class="sxs-lookup"><span data-stu-id="8d252-103">Adds SSH public keys to the VMSS.</span></span>

## <span data-ttu-id="8d252-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8d252-104">SYNTAX</span></span>

```
Add-AzVmssSshPublicKey [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Path] <String>]
 [[-KeyData] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8d252-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8d252-105">DESCRIPTION</span></span>
<span data-ttu-id="8d252-106">Das **Add-AzVmssSshPublicKey-Cmdlet** fügt die öffentlichen Schlüssel hinzu, die Sie verwenden können, um über Secure Shell (SSH) eine Verbindung mit virtuellen VmSS (Virtual Machine Scale Set) herzustellen.</span><span class="sxs-lookup"><span data-stu-id="8d252-106">The **Add-AzVmssSshPublicKey** cmdlet adds the public keys that you can use to connect to the Virtual Machine Scale Set (VMSS) virtual machines over Secure Shell (SSH).</span></span>

## <span data-ttu-id="8d252-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8d252-107">EXAMPLES</span></span>

### <span data-ttu-id="8d252-108">Beispiel 1: Hinzufügen eines öffentlichen SSH-Schlüssels zum VMSS</span><span class="sxs-lookup"><span data-stu-id="8d252-108">Example 1: Add an SSH public key to the VMSS</span></span>
```
PS C:\> $VMSS = New-AzVmssConfig
PS C:\> Add-AzVmssSshPublicKey -VirtualMachineScaleSet $VMSS -KeyData "MIIDszCCApugAwIBAgIJALBV9YJCF/tAMA0GCSq12Ib3DQEB21QUAMEUxCzAJBgNV" -Path "/home/admin/.ssh/authorized_keys"
```

<span data-ttu-id="8d252-109">In diesem Beispiel wird dem VMSS ein öffentlicher SSH-Schlüssel hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="8d252-109">This example adds an SSH public key to the VMSS.</span></span>
<span data-ttu-id="8d252-110">Der erste Befehl verwendet das **Cmdlet New-AzVmssConfig** zum Erstellen eines VMSS-Konfigurationsobjekts und speichert das Ergebnis in der Variablen namens $VMSS.</span><span class="sxs-lookup"><span data-stu-id="8d252-110">The first command uses the **New-AzVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
<span data-ttu-id="8d252-111">Der zweite Befehl fügt einen SSH-Schlüssel mit den angegebenen Schlüsseldaten hinzu und speichert den Schlüssel am angegebenen Pfad auf dem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="8d252-111">The second command adds an SSH key with the specified key data and stores the key at the specified path on the virtual machine.</span></span>

## <span data-ttu-id="8d252-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="8d252-112">PARAMETERS</span></span>

### <span data-ttu-id="8d252-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d252-113">-DefaultProfile</span></span>
<span data-ttu-id="8d252-114">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8d252-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8d252-115">-KeyData</span><span class="sxs-lookup"><span data-stu-id="8d252-115">-KeyData</span></span>
<span data-ttu-id="8d252-116">Gibt einen öffentlichen SSH RSA-Schlüssel an.</span><span class="sxs-lookup"><span data-stu-id="8d252-116">Specifies a SSH RSA public key data.</span></span>

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

### <span data-ttu-id="8d252-117">-Path</span><span class="sxs-lookup"><span data-stu-id="8d252-117">-Path</span></span>
<span data-ttu-id="8d252-118">Gibt den vollständigen Pfad einer Datei auf dem virtuellen Computer an, auf dem dieses Cmdlet den öffentlichen SSH-Schlüssel speichert.</span><span class="sxs-lookup"><span data-stu-id="8d252-118">Specifies the full path of a file, on the virtual machine, where this cmdlet stores the SSH public key.</span></span>
<span data-ttu-id="8d252-119">Wenn die Datei bereits vorhanden ist, fügt dieses Cmdlet den Schlüssel an die Datei an.</span><span class="sxs-lookup"><span data-stu-id="8d252-119">If the file already exists, this cmdlet appends the key to the file.</span></span>

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

### <span data-ttu-id="8d252-120">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="8d252-120">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="8d252-121">Gibt das VMSS-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="8d252-121">Specifies the VMSS object.</span></span>
<span data-ttu-id="8d252-122">Sie können das [Cmdlet New-AzVmssConfig](./New-AzVmssConfig.md) verwenden, um das -Objekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="8d252-122">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) cmdlet to create the object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8d252-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8d252-123">-Confirm</span></span>
<span data-ttu-id="8d252-124">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8d252-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d252-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8d252-125">-WhatIf</span></span>
<span data-ttu-id="8d252-126">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8d252-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8d252-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8d252-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d252-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d252-128">CommonParameters</span></span>
<span data-ttu-id="8d252-129">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d252-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d252-130">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8d252-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d252-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8d252-131">INPUTS</span></span>

### <span data-ttu-id="8d252-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="8d252-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="8d252-133">System.String</span><span class="sxs-lookup"><span data-stu-id="8d252-133">System.String</span></span>

## <span data-ttu-id="8d252-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8d252-134">OUTPUTS</span></span>

### <span data-ttu-id="8d252-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="8d252-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="8d252-136">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="8d252-136">NOTES</span></span>

## <span data-ttu-id="8d252-137">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="8d252-137">RELATED LINKS</span></span>

[<span data-ttu-id="8d252-138">New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="8d252-138">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)
