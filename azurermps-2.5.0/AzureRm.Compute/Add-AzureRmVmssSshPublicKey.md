---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 9C216103-EB77-468E-8684-F5E5400B73A7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/add-azurermvmsssshpublickey
schema: 2.0.0
ms.openlocfilehash: 6cd715c3ba6ef0a890f5aaeaf04022b19026592c
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848935"
---
# <span data-ttu-id="8fef2-101">Add-AzureRmVmssSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="8fef2-101">Add-AzureRmVmssSshPublicKey</span></span>

## <span data-ttu-id="8fef2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8fef2-102">SYNOPSIS</span></span>
<span data-ttu-id="8fef2-103">Fügt dem VMSS SSH-öffentliche Schlüssel hinzu.</span><span class="sxs-lookup"><span data-stu-id="8fef2-103">Adds SSH public keys to the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8fef2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8fef2-104">SYNTAX</span></span>

```
Add-AzureRmVmssSshPublicKey [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Path] <String>]
 [[-KeyData] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8fef2-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8fef2-105">DESCRIPTION</span></span>
<span data-ttu-id="8fef2-106">Mit dem Cmdlet **Add-AzureRmVmssSshPublicKey** werden die öffentlichen Schlüssel hinzugefügt, mit denen Sie eine Verbindung mit den virtuellen Computern des virtuellen Computers Scale-Sets (VMSS) über Secure Shell (SSH) herstellen können.</span><span class="sxs-lookup"><span data-stu-id="8fef2-106">The **Add-AzureRmVmssSshPublicKey** cmdlet adds the public keys that you can use to connect to the Virtual Machine Scale Set (VMSS) virtual machines over Secure Shell (SSH).</span></span>

## <span data-ttu-id="8fef2-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8fef2-107">EXAMPLES</span></span>

### <span data-ttu-id="8fef2-108">Beispiel 1: Hinzufügen eines öffentlichen SSH-Schlüssels zum VMSS</span><span class="sxs-lookup"><span data-stu-id="8fef2-108">Example 1: Add an SSH public key to the VMSS</span></span>
```
PS C:\> $VMSS = New-AzureRmVmssConfig
PS C:\> Add-AzureRmVmssSshPublicKey -VirtualMachineScaleSet $VMSS -KeyData "MIIDszCCApugAwIBAgIJALBV9YJCF/tAMA0GCSq12Ib3DQEB21QUAMEUxCzAJBgNV" -Path "/home/admin/.ssh/authorized_keys"
```

<span data-ttu-id="8fef2-109">In diesem Beispiel wird ein öffentlicher SSH-Schlüssel zum VMSS hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="8fef2-109">This example adds an SSH public key to the VMSS.</span></span>

<span data-ttu-id="8fef2-110">Der erste Befehl verwendet das Cmdlet **New-AzureRmVmssConfig** , um ein VMSS-Konfigurationsobjekt zu erstellen und das Ergebnis in der Variablen mit dem Namen $VMSS zu speichern.</span><span class="sxs-lookup"><span data-stu-id="8fef2-110">The first command uses the **New-AzureRmVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
<span data-ttu-id="8fef2-111">Der zweite Befehl fügt einen SSH-Schlüssel mit den angegebenen Schlüsseldaten hinzu und speichert den Schlüssel am angegebenen Pfad auf dem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="8fef2-111">The second command adds an SSH key with the specified key data and stores the key at the specified path on the virtual machine.</span></span>

## <span data-ttu-id="8fef2-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="8fef2-112">PARAMETERS</span></span>

### <span data-ttu-id="8fef2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8fef2-113">-DefaultProfile</span></span>
<span data-ttu-id="8fef2-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8fef2-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8fef2-115">-KeyData</span><span class="sxs-lookup"><span data-stu-id="8fef2-115">-KeyData</span></span>
<span data-ttu-id="8fef2-116">Gibt einen SSH-RSA-Public-Key-Daten an.</span><span class="sxs-lookup"><span data-stu-id="8fef2-116">Specifies a SSH RSA public key data.</span></span>

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

### <span data-ttu-id="8fef2-117">-Path</span><span class="sxs-lookup"><span data-stu-id="8fef2-117">-Path</span></span>
<span data-ttu-id="8fef2-118">Gibt den vollständigen Pfad einer Datei auf dem virtuellen Computer an, in dem dieses Cmdlet den öffentlichen SSH-Schlüssel speichert.</span><span class="sxs-lookup"><span data-stu-id="8fef2-118">Specifies the full path of a file, on the virtual machine, where this cmdlet stores the SSH public key.</span></span>
<span data-ttu-id="8fef2-119">Wenn die Datei bereits vorhanden ist, hängt dieses Cmdlet den Schlüssel an die Datei an.</span><span class="sxs-lookup"><span data-stu-id="8fef2-119">If the file already exists, this cmdlet appends the key to the file.</span></span>

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

### <span data-ttu-id="8fef2-120">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="8fef2-120">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="8fef2-121">Gibt das VMSS-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="8fef2-121">Specifies the VMSS object.</span></span>
<span data-ttu-id="8fef2-122">Sie können das Cmdlet [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) verwenden, um das Objekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="8fef2-122">You can use the [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) cmdlet to create the object.</span></span>

```yaml
Type: PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8fef2-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8fef2-123">-Confirm</span></span>
<span data-ttu-id="8fef2-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8fef2-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fef2-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8fef2-125">-WhatIf</span></span>
<span data-ttu-id="8fef2-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8fef2-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8fef2-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8fef2-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fef2-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8fef2-128">CommonParameters</span></span>
<span data-ttu-id="8fef2-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8fef2-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8fef2-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8fef2-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8fef2-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8fef2-131">INPUTS</span></span>

### <span data-ttu-id="8fef2-132">VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="8fef2-132">VirtualMachineScaleSet</span></span>
<span data-ttu-id="8fef2-133">Der Parameter "VirtualMachineScaleSet" akzeptiert den Wert vom Typ "VirtualMachineScaleSet" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="8fef2-133">Parameter 'VirtualMachineScaleSet' accepts value of type 'VirtualMachineScaleSet' from the pipeline</span></span>

## <span data-ttu-id="8fef2-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8fef2-134">OUTPUTS</span></span>

###  
<span data-ttu-id="8fef2-135">Dieses Cmdlet generiert keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="8fef2-135">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="8fef2-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="8fef2-136">NOTES</span></span>

## <span data-ttu-id="8fef2-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8fef2-137">RELATED LINKS</span></span>

[<span data-ttu-id="8fef2-138">Neu – AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="8fef2-138">New-AzureRmVmssConfig</span></span>](./New-AzureRmVmssConfig.md)
