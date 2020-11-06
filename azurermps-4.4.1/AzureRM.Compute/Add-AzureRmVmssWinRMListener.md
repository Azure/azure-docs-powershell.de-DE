---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 987BD670-20F3-4105-A5BE-03E712AB2B56
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssWinRMListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssWinRMListener.md
ms.openlocfilehash: 77cefdacfee2e2c8cb1e0d5508a418cf6bbafcbe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505205"
---
# <span data-ttu-id="15dc4-101">Add-AzureRmVmssWinRMListener</span><span class="sxs-lookup"><span data-stu-id="15dc4-101">Add-AzureRmVmssWinRMListener</span></span>

## <span data-ttu-id="15dc4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="15dc4-102">SYNOPSIS</span></span>
<span data-ttu-id="15dc4-103">Fügt der VMSS einen WinRM-Listener hinzu.</span><span class="sxs-lookup"><span data-stu-id="15dc4-103">Adds a WinRM listener to the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="15dc4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="15dc4-104">SYNTAX</span></span>

```
Add-AzureRmVmssWinRMListener [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Protocol] <ProtocolTypes>]
 [[-CertificateUrl] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="15dc4-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="15dc4-105">DESCRIPTION</span></span>
<span data-ttu-id="15dc4-106">Mit dem Cmdlet " **Add-AzureRmVmssWinRMListener** " wird ein Windows Remote Management (WinRM)-Listener auf dem virtuellen Computer-Skalierungs Satz (VMSS) hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="15dc4-106">The **Add-AzureRmVmssWinRMListener** cmdlet adds a Windows Remote Management (WinRM) listener on the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="15dc4-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="15dc4-107">EXAMPLES</span></span>

### <span data-ttu-id="15dc4-108">Beispiel 1: Hinzufügen eines WinRM-Listeners zum VMSS</span><span class="sxs-lookup"><span data-stu-id="15dc4-108">Example 1: Add a WinRM listener to the VMSS</span></span>
```
PS C:\> $VMSS = New-AzureRmVmssConfig
PS C:\> Add-AzureRmVmssWinRMListener -VirtualMachineScaleSet $VMSS -Protocol Https -CertificateUrl "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion"
```

<span data-ttu-id="15dc4-109">In diesem Beispiel wird der VMSS ein WinRM-Listener hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="15dc4-109">This example adds a WinRM listener to the VMSS.</span></span>

<span data-ttu-id="15dc4-110">Der erste Befehl verwendet das Cmdlet **New-AzureRmVmssConfig** , um ein VMSS-Konfigurationsobjekt zu erstellen und das Ergebnis in der Variablen mit dem Namen $VMSS zu speichern.</span><span class="sxs-lookup"><span data-stu-id="15dc4-110">The first command uses the **New-AzureRmVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
<span data-ttu-id="15dc4-111">Mit dem zweiten Befehl wird ein HTTP-Protokoll WinRM-Listener mit dem Zertifikat an der angegebenen URL zum VMSS hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="15dc4-111">The second command adds an HTTP protocol WinRM listener with the certificate at the specified URL to the VMSS.</span></span>

## <span data-ttu-id="15dc4-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="15dc4-112">PARAMETERS</span></span>

### <span data-ttu-id="15dc4-113">-CertificateUrl</span><span class="sxs-lookup"><span data-stu-id="15dc4-113">-CertificateUrl</span></span>
<span data-ttu-id="15dc4-114">Gibt einen Link als URL des Zertifikats an, mit dem neue virtuelle Computer bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="15dc4-114">Specifies a link, as a URL, of the certificate with which new virtual machines are provisioned.</span></span>

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

### <span data-ttu-id="15dc4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15dc4-115">-DefaultProfile</span></span>
<span data-ttu-id="15dc4-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="15dc4-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15dc4-117">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="15dc4-117">-Protocol</span></span>
<span data-ttu-id="15dc4-118">Gibt das Protokoll des WinRM-Listener an.</span><span class="sxs-lookup"><span data-stu-id="15dc4-118">Specifies the protocol of the WinRM listener.</span></span>
<span data-ttu-id="15dc4-119">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="15dc4-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="15dc4-120">Http</span><span class="sxs-lookup"><span data-stu-id="15dc4-120">Http</span></span>
- <span data-ttu-id="15dc4-121">HTTPS</span><span class="sxs-lookup"><span data-stu-id="15dc4-121">Https</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.ProtocolTypes]
Parameter Sets: (All)
Aliases: 
Accepted values: Http, Https

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15dc4-122">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="15dc4-122">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="15dc4-123">Gibt das VMSS-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="15dc4-123">Specifies the VMSS object.</span></span>
<span data-ttu-id="15dc4-124">Sie können das New-AzureRmVmssConfig-Cmdlet verwenden, um das Objekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="15dc4-124">You can use the New-AzureRmVmssConfig cmdlet to create the object.</span></span>

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

### <span data-ttu-id="15dc4-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="15dc4-125">-Confirm</span></span>
<span data-ttu-id="15dc4-126">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="15dc4-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="15dc4-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="15dc4-127">-WhatIf</span></span>
<span data-ttu-id="15dc4-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="15dc4-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="15dc4-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="15dc4-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="15dc4-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15dc4-130">CommonParameters</span></span>
<span data-ttu-id="15dc4-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="15dc4-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15dc4-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="15dc4-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15dc4-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="15dc4-133">INPUTS</span></span>

## <span data-ttu-id="15dc4-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="15dc4-134">OUTPUTS</span></span>

### <span data-ttu-id="15dc4-135">Dieses Cmdlet generiert keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="15dc4-135">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="15dc4-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="15dc4-136">NOTES</span></span>

## <span data-ttu-id="15dc4-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="15dc4-137">RELATED LINKS</span></span>

[<span data-ttu-id="15dc4-138">Neu – AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="15dc4-138">New-AzureRmVmssConfig</span></span>](./New-AzureRmVmssConfig.md)


