---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 987BD670-20F3-4105-A5BE-03E712AB2B56
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmsswinrmlistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Add-AzVmssWinRMListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Add-AzVmssWinRMListener.md
ms.openlocfilehash: 00e61142948e42310dbd5c0be56660c17ec7e8e3
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844703"
---
# <span data-ttu-id="61f2e-101">Add-AzVmssWinRMListener</span><span class="sxs-lookup"><span data-stu-id="61f2e-101">Add-AzVmssWinRMListener</span></span>

## <span data-ttu-id="61f2e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="61f2e-102">SYNOPSIS</span></span>
<span data-ttu-id="61f2e-103">Fügt der VMSS einen WinRM-Listener hinzu.</span><span class="sxs-lookup"><span data-stu-id="61f2e-103">Adds a WinRM listener to the VMSS.</span></span>

## <span data-ttu-id="61f2e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="61f2e-104">SYNTAX</span></span>

```
Add-AzVmssWinRMListener [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Protocol] <ProtocolTypes>]
 [[-CertificateUrl] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="61f2e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="61f2e-105">DESCRIPTION</span></span>
<span data-ttu-id="61f2e-106">Mit dem Cmdlet " **Add-AzVmssWinRMListener** " wird ein Windows Remote Management (WinRM)-Listener auf dem virtuellen Computer-Skalierungs Satz (VMSS) hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="61f2e-106">The **Add-AzVmssWinRMListener** cmdlet adds a Windows Remote Management (WinRM) listener on the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="61f2e-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="61f2e-107">EXAMPLES</span></span>

### <span data-ttu-id="61f2e-108">Beispiel 1: Hinzufügen eines WinRM-Listeners zum VMSS</span><span class="sxs-lookup"><span data-stu-id="61f2e-108">Example 1: Add a WinRM listener to the VMSS</span></span>
```
PS C:\> $VMSS = New-AzVmssConfig
PS C:\> Add-AzVmssWinRMListener -VirtualMachineScaleSet $VMSS -Protocol Https -CertificateUrl "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion"
```

<span data-ttu-id="61f2e-109">In diesem Beispiel wird der VMSS ein WinRM-Listener hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="61f2e-109">This example adds a WinRM listener to the VMSS.</span></span>

<span data-ttu-id="61f2e-110">Der erste Befehl verwendet das Cmdlet **New-AzVmssConfig** , um ein VMSS-Konfigurationsobjekt zu erstellen und das Ergebnis in der Variablen mit dem Namen $VMSS zu speichern.</span><span class="sxs-lookup"><span data-stu-id="61f2e-110">The first command uses the **New-AzVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
<span data-ttu-id="61f2e-111">Mit dem zweiten Befehl wird ein HTTP-Protokoll WinRM-Listener mit dem Zertifikat an der angegebenen URL zum VMSS hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="61f2e-111">The second command adds an HTTP protocol WinRM listener with the certificate at the specified URL to the VMSS.</span></span>

## <span data-ttu-id="61f2e-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="61f2e-112">PARAMETERS</span></span>

### <span data-ttu-id="61f2e-113">-CertificateUrl</span><span class="sxs-lookup"><span data-stu-id="61f2e-113">-CertificateUrl</span></span>
<span data-ttu-id="61f2e-114">Gibt einen Link als URL des Zertifikats an, mit dem neue virtuelle Computer bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="61f2e-114">Specifies a link, as a URL, of the certificate with which new virtual machines are provisioned.</span></span>

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

### <span data-ttu-id="61f2e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61f2e-115">-DefaultProfile</span></span>
<span data-ttu-id="61f2e-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="61f2e-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="61f2e-117">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="61f2e-117">-Protocol</span></span>
<span data-ttu-id="61f2e-118">Gibt das Protokoll des WinRM-Listener an.</span><span class="sxs-lookup"><span data-stu-id="61f2e-118">Specifies the protocol of the WinRM listener.</span></span>
<span data-ttu-id="61f2e-119">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="61f2e-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="61f2e-120">Http</span><span class="sxs-lookup"><span data-stu-id="61f2e-120">Http</span></span>
- <span data-ttu-id="61f2e-121">HTTPS</span><span class="sxs-lookup"><span data-stu-id="61f2e-121">Https</span></span>

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

### <span data-ttu-id="61f2e-122">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="61f2e-122">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="61f2e-123">Gibt das VMSS-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="61f2e-123">Specifies the VMSS object.</span></span>
<span data-ttu-id="61f2e-124">Sie können das New-AzVmssConfig-Cmdlet verwenden, um das Objekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="61f2e-124">You can use the New-AzVmssConfig cmdlet to create the object.</span></span>

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

### <span data-ttu-id="61f2e-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="61f2e-125">-Confirm</span></span>
<span data-ttu-id="61f2e-126">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="61f2e-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="61f2e-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61f2e-127">-WhatIf</span></span>
<span data-ttu-id="61f2e-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="61f2e-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="61f2e-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="61f2e-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="61f2e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61f2e-130">CommonParameters</span></span>
<span data-ttu-id="61f2e-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61f2e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61f2e-132">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61f2e-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61f2e-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="61f2e-133">INPUTS</span></span>

### <span data-ttu-id="61f2e-134">VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="61f2e-134">VirtualMachineScaleSet</span></span>
<span data-ttu-id="61f2e-135">Der Parameter "VirtualMachineScaleSet" akzeptiert den Wert vom Typ "VirtualMachineScaleSet" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="61f2e-135">Parameter 'VirtualMachineScaleSet' accepts value of type 'VirtualMachineScaleSet' from the pipeline</span></span>

## <span data-ttu-id="61f2e-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="61f2e-136">OUTPUTS</span></span>

### <span data-ttu-id="61f2e-137">Dieses Cmdlet generiert keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="61f2e-137">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="61f2e-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="61f2e-138">NOTES</span></span>

## <span data-ttu-id="61f2e-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="61f2e-139">RELATED LINKS</span></span>

[<span data-ttu-id="61f2e-140">Neu – AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="61f2e-140">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)


