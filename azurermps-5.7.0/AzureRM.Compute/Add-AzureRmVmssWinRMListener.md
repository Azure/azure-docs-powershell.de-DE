---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 987BD670-20F3-4105-A5BE-03E712AB2B56
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssWinRMListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssWinRMListener.md
ms.openlocfilehash: d2ed576131ad2ff33ae7e5c7e5be091ca8f4a50e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93476986"
---
# <span data-ttu-id="42138-101">Add-AzureRmVmssWinRMListener</span><span class="sxs-lookup"><span data-stu-id="42138-101">Add-AzureRmVmssWinRMListener</span></span>

## <span data-ttu-id="42138-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="42138-102">SYNOPSIS</span></span>
<span data-ttu-id="42138-103">Fügt der VMSS einen WinRM-Listener hinzu.</span><span class="sxs-lookup"><span data-stu-id="42138-103">Adds a WinRM listener to the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="42138-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="42138-104">SYNTAX</span></span>

```
Add-AzureRmVmssWinRMListener [-VirtualMachineScaleSet] <VirtualMachineScaleSet> [[-Protocol] <ProtocolTypes>]
 [[-CertificateUrl] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="42138-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="42138-105">DESCRIPTION</span></span>
<span data-ttu-id="42138-106">Mit dem Cmdlet " **Add-AzureRmVmssWinRMListener** " wird ein Windows Remote Management (WinRM)-Listener auf dem virtuellen Computer-Skalierungs Satz (VMSS) hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="42138-106">The **Add-AzureRmVmssWinRMListener** cmdlet adds a Windows Remote Management (WinRM) listener on the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="42138-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="42138-107">EXAMPLES</span></span>

### <span data-ttu-id="42138-108">Beispiel 1: Hinzufügen eines WinRM-Listeners zum VMSS</span><span class="sxs-lookup"><span data-stu-id="42138-108">Example 1: Add a WinRM listener to the VMSS</span></span>
```
PS C:\> $VMSS = New-AzureRmVmssConfig
PS C:\> Add-AzureRmVmssWinRMListener -VirtualMachineScaleSet $VMSS -Protocol Https -CertificateUrl "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion"
```

<span data-ttu-id="42138-109">In diesem Beispiel wird der VMSS ein WinRM-Listener hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="42138-109">This example adds a WinRM listener to the VMSS.</span></span>

<span data-ttu-id="42138-110">Der erste Befehl verwendet das Cmdlet **New-AzureRmVmssConfig** , um ein VMSS-Konfigurationsobjekt zu erstellen und das Ergebnis in der Variablen mit dem Namen $VMSS zu speichern.</span><span class="sxs-lookup"><span data-stu-id="42138-110">The first command uses the **New-AzureRmVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
<span data-ttu-id="42138-111">Mit dem zweiten Befehl wird ein HTTP-Protokoll WinRM-Listener mit dem Zertifikat an der angegebenen URL zum VMSS hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="42138-111">The second command adds an HTTP protocol WinRM listener with the certificate at the specified URL to the VMSS.</span></span>

## <span data-ttu-id="42138-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="42138-112">PARAMETERS</span></span>

### <span data-ttu-id="42138-113">-CertificateUrl</span><span class="sxs-lookup"><span data-stu-id="42138-113">-CertificateUrl</span></span>
<span data-ttu-id="42138-114">Gibt einen Link als URL des Zertifikats an, mit dem neue virtuelle Computer bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="42138-114">Specifies a link, as a URL, of the certificate with which new virtual machines are provisioned.</span></span>

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

### <span data-ttu-id="42138-115">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="42138-115">-Protocol</span></span>
<span data-ttu-id="42138-116">Gibt das Protokoll des WinRM-Listener an.</span><span class="sxs-lookup"><span data-stu-id="42138-116">Specifies the protocol of the WinRM listener.</span></span>
<span data-ttu-id="42138-117">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="42138-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="42138-118">Http</span><span class="sxs-lookup"><span data-stu-id="42138-118">Http</span></span>
- <span data-ttu-id="42138-119">HTTPS</span><span class="sxs-lookup"><span data-stu-id="42138-119">Https</span></span>

```yaml
Type: ProtocolTypes
Parameter Sets: (All)
Aliases: 
Accepted values: Http, Https

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42138-120">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="42138-120">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="42138-121">Gibt das VMSS-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="42138-121">Specifies the VMSS object.</span></span>
<span data-ttu-id="42138-122">Sie können das New-AzureRmVmssConfig-Cmdlet verwenden, um das Objekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="42138-122">You can use the New-AzureRmVmssConfig cmdlet to create the object.</span></span>

```yaml
Type: VirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="42138-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="42138-123">-Confirm</span></span>
<span data-ttu-id="42138-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="42138-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="42138-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="42138-125">-WhatIf</span></span>
<span data-ttu-id="42138-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="42138-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="42138-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="42138-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="42138-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42138-128">CommonParameters</span></span>
<span data-ttu-id="42138-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42138-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42138-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42138-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42138-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="42138-131">INPUTS</span></span>

### <span data-ttu-id="42138-132">Keine</span><span class="sxs-lookup"><span data-stu-id="42138-132">None</span></span>
<span data-ttu-id="42138-133">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="42138-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="42138-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="42138-134">OUTPUTS</span></span>

### <span data-ttu-id="42138-135">Dieses Cmdlet generiert keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="42138-135">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="42138-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="42138-136">NOTES</span></span>

## <span data-ttu-id="42138-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="42138-137">RELATED LINKS</span></span>

[<span data-ttu-id="42138-138">Neu – AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="42138-138">New-AzureRmVmssConfig</span></span>](./New-AzureRmVmssConfig.md)


