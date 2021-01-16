---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 987BD670-20F3-4105-A5BE-03E712AB2B56
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmsswinrmlistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssWinRMListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssWinRMListener.md
ms.openlocfilehash: 471baa126cd58bb241fa6b8da358769d09be3f20
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98293566"
---
# <span data-ttu-id="ad0e0-101">Add-AzVmssWinRMListener</span><span class="sxs-lookup"><span data-stu-id="ad0e0-101">Add-AzVmssWinRMListener</span></span>

## <span data-ttu-id="ad0e0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ad0e0-102">SYNOPSIS</span></span>
<span data-ttu-id="ad0e0-103">Fügt der VMSS einen "WinRM"-Listener hinzu.</span><span class="sxs-lookup"><span data-stu-id="ad0e0-103">Adds a WinRM listener to the VMSS.</span></span>

## <span data-ttu-id="ad0e0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ad0e0-104">SYNTAX</span></span>

```
Add-AzVmssWinRMListener [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Protocol] <ProtocolTypes>]
 [[-CertificateUrl] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ad0e0-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ad0e0-105">DESCRIPTION</span></span>
<span data-ttu-id="ad0e0-106">Das **Cmdlet "Add-AzVmssWinRMListener"** fügt dem Virtual Machine Scale Set (VMSS) einen Windows Remote Management (WinRM)-Listener hinzu.</span><span class="sxs-lookup"><span data-stu-id="ad0e0-106">The **Add-AzVmssWinRMListener** cmdlet adds a Windows Remote Management (WinRM) listener on the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="ad0e0-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ad0e0-107">EXAMPLES</span></span>

### <span data-ttu-id="ad0e0-108">Beispiel 1: Hinzufügen eines WinRM-Listeners zu VMSS</span><span class="sxs-lookup"><span data-stu-id="ad0e0-108">Example 1: Add a WinRM listener to the VMSS</span></span>
```
PS C:\> $VMSS = New-AzVmssConfig
PS C:\> Add-AzVmssWinRMListener -VirtualMachineScaleSet $VMSS -Protocol Https -CertificateUrl "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion"
```

<span data-ttu-id="ad0e0-109">In diesem Beispiel wird der VMSS ein WinRM-Listener hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="ad0e0-109">This example adds a WinRM listener to the VMSS.</span></span>
<span data-ttu-id="ad0e0-110">Der erste Befehl verwendet das **Cmdlet "New-AzVmssConfig"** zum Erstellen eines VMSS-Konfigurationsobjekts und speichert das Ergebnis in der Variablen namens $VMSS.</span><span class="sxs-lookup"><span data-stu-id="ad0e0-110">The first command uses the **New-AzVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
<span data-ttu-id="ad0e0-111">Der zweite Befehl fügt dem VMSS einen HTTP-Protokoll-WinRM-Listener mit dem Zertifikat unter der angegebenen URL hinzu.</span><span class="sxs-lookup"><span data-stu-id="ad0e0-111">The second command adds an HTTP protocol WinRM listener with the certificate at the specified URL to the VMSS.</span></span>

## <span data-ttu-id="ad0e0-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ad0e0-112">PARAMETERS</span></span>

### <span data-ttu-id="ad0e0-113">-CertificateUrl</span><span class="sxs-lookup"><span data-stu-id="ad0e0-113">-CertificateUrl</span></span>
<span data-ttu-id="ad0e0-114">Gibt einen Link (als URL) des Zertifikats an, mit dem neue virtuelle Computer bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="ad0e0-114">Specifies a link, as a URL, of the certificate with which new virtual machines are provisioned.</span></span>

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

### <span data-ttu-id="ad0e0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad0e0-115">-DefaultProfile</span></span>
<span data-ttu-id="ad0e0-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ad0e0-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ad0e0-117">-Protocol</span><span class="sxs-lookup"><span data-stu-id="ad0e0-117">-Protocol</span></span>
<span data-ttu-id="ad0e0-118">Gibt das Protokoll des WinRM-Listeners an.</span><span class="sxs-lookup"><span data-stu-id="ad0e0-118">Specifies the protocol of the WinRM listener.</span></span>
<span data-ttu-id="ad0e0-119">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="ad0e0-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ad0e0-120">Http</span><span class="sxs-lookup"><span data-stu-id="ad0e0-120">Http</span></span>
- <span data-ttu-id="ad0e0-121">Https</span><span class="sxs-lookup"><span data-stu-id="ad0e0-121">Https</span></span>

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

### <span data-ttu-id="ad0e0-122">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="ad0e0-122">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="ad0e0-123">Gibt das "VMSS"-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="ad0e0-123">Specifies the VMSS object.</span></span>
<span data-ttu-id="ad0e0-124">Sie können das cmdlet New-AzVmssConfig zum Erstellen des Objekts verwenden.</span><span class="sxs-lookup"><span data-stu-id="ad0e0-124">You can use the New-AzVmssConfig cmdlet to create the object.</span></span>

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

### <span data-ttu-id="ad0e0-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ad0e0-125">-Confirm</span></span>
<span data-ttu-id="ad0e0-126">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ad0e0-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad0e0-127">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="ad0e0-127">-WhatIf</span></span>
<span data-ttu-id="ad0e0-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ad0e0-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ad0e0-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ad0e0-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad0e0-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad0e0-130">CommonParameters</span></span>
<span data-ttu-id="ad0e0-131">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad0e0-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad0e0-132">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ad0e0-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad0e0-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ad0e0-133">INPUTS</span></span>

### <span data-ttu-id="ad0e0-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="ad0e0-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="ad0e0-135">System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.ProtocolTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="ad0e0-135">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.ProtocolTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="ad0e0-136">System.String</span><span class="sxs-lookup"><span data-stu-id="ad0e0-136">System.String</span></span>

## <span data-ttu-id="ad0e0-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ad0e0-137">OUTPUTS</span></span>

### <span data-ttu-id="ad0e0-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="ad0e0-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="ad0e0-139">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="ad0e0-139">NOTES</span></span>

## <span data-ttu-id="ad0e0-140">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="ad0e0-140">RELATED LINKS</span></span>

[<span data-ttu-id="ad0e0-141">New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="ad0e0-141">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)


