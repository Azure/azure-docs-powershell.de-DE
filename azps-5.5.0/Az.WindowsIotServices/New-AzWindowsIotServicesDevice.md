---
external help file: ''
Module Name: Az.WindowsIotServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.windowsiotservices/new-azwindowsiotservicesdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/WindowsIotServices/help/New-AzWindowsIotServicesDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/WindowsIotServices/help/New-AzWindowsIotServicesDevice.md
ms.openlocfilehash: 4da60a6d4083992f843121cb141a453b4ef3b4b8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100173337"
---
# <span data-ttu-id="f3ed7-101">New-AzWindowsIotServicesDevice</span><span class="sxs-lookup"><span data-stu-id="f3ed7-101">New-AzWindowsIotServicesDevice</span></span>

## <span data-ttu-id="f3ed7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f3ed7-102">SYNOPSIS</span></span>
<span data-ttu-id="f3ed7-103">Erstellen oder aktualisieren Sie die Metadaten eines Windows IoT-Gerätediensts.</span><span class="sxs-lookup"><span data-stu-id="f3ed7-103">Create or update the metadata of a Windows IoT Device Service.</span></span>
<span data-ttu-id="f3ed7-104">Das übliche Muster zum Ändern einer Eigenschaft besteht im Abrufen der Windows IoT-Gerätedienstmetadaten und Sicherheitsmetadaten, die dann mit den geänderten Werten in einem neuen Textkörper kombiniert werden, um den Windows IoT-Gerätedienst zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="f3ed7-104">The usual pattern to modify a property is to retrieve the Windows IoT Device Service metadata and security metadata, and then combine them with the modified values in a new body to update the Windows IoT Device Service.</span></span>

## <span data-ttu-id="f3ed7-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f3ed7-105">SYNTAX</span></span>

```
New-AzWindowsIotServicesDevice -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-IfMatch <String>] [-AdminDomainName <String>] [-BillingDomainName <String>] [-Etag <String>]
 [-Location <String>] [-Note <String>] [-Quantity <Int64>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f3ed7-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f3ed7-106">DESCRIPTION</span></span>
<span data-ttu-id="f3ed7-107">Erstellen oder aktualisieren Sie die Metadaten eines Windows IoT-Gerätediensts.</span><span class="sxs-lookup"><span data-stu-id="f3ed7-107">Create or update the metadata of a Windows IoT Device Service.</span></span>
<span data-ttu-id="f3ed7-108">Das übliche Muster zum Ändern einer Eigenschaft besteht im Abrufen der Windows IoT-Gerätedienstmetadaten und Sicherheitsmetadaten, die dann mit den geänderten Werten in einem neuen Textkörper kombiniert werden, um den Windows IoT-Gerätedienst zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="f3ed7-108">The usual pattern to modify a property is to retrieve the Windows IoT Device Service metadata and security metadata, and then combine them with the modified values in a new body to update the Windows IoT Device Service.</span></span>

## <span data-ttu-id="f3ed7-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f3ed7-109">EXAMPLES</span></span>

### <span data-ttu-id="f3ed7-110">Beispiel 1: Erstellen neuer Windows -IoT-Dienste</span><span class="sxs-lookup"><span data-stu-id="f3ed7-110">Example 1: Create a new Windows IoT services</span></span>
```powershell
PS C:\> New-AzWindowsIotServicesDevice -Name wsi-t03 -ResourceGroupName azure-rg-test -Location eastus -Quantity 10 -BillingDomainName 'microsoft.onmicrosoft.com' -AdminDomainName 'microsoft.onmicrosoft.com'

Location Name    Type                                Etag
-------- ----    ----                                ----
eastus   wsi-t03 Microsoft.WindowsIoT/DeviceServices "6a00eee9-0000-0700-0000-5fab82870000"
```

<span data-ttu-id="f3ed7-111">Mit diesem Befehl werden neue Windows IoT-Dienste erstellt.</span><span class="sxs-lookup"><span data-stu-id="f3ed7-111">This command creates a new Windows IoT services.</span></span>

## <span data-ttu-id="f3ed7-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f3ed7-112">PARAMETERS</span></span>

### <span data-ttu-id="f3ed7-113">-AdminDomainName</span><span class="sxs-lookup"><span data-stu-id="f3ed7-113">-AdminDomainName</span></span>
<span data-ttu-id="f3ed7-114">Oem-AAD-Domäne des Windows IoT-Gerätediensts</span><span class="sxs-lookup"><span data-stu-id="f3ed7-114">Windows IoT Device Service OEM AAD domain</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3ed7-115">-BillingDomainName</span><span class="sxs-lookup"><span data-stu-id="f3ed7-115">-BillingDomainName</span></span>
<span data-ttu-id="f3ed7-116">Windows IoT Device Service ODM AAD domain</span><span class="sxs-lookup"><span data-stu-id="f3ed7-116">Windows IoT Device Service ODM AAD domain</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3ed7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3ed7-117">-DefaultProfile</span></span>
<span data-ttu-id="f3ed7-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f3ed7-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3ed7-119">-Etag</span><span class="sxs-lookup"><span data-stu-id="f3ed7-119">-Etag</span></span>
<span data-ttu-id="f3ed7-120">Das #A0 ist *nicht* erforderlich.</span><span class="sxs-lookup"><span data-stu-id="f3ed7-120">The Etag field is *not* required.</span></span>
<span data-ttu-id="f3ed7-121">Wenn sie im Antworttext bereitgestellt wird, muss sie auch als Kopfzeile nach der normalen #A0 bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="f3ed7-121">If it is provided in the response body, it must also be provided as a header per the normal ETag convention.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3ed7-122">-IfMatch</span><span class="sxs-lookup"><span data-stu-id="f3ed7-122">-IfMatch</span></span>
<span data-ttu-id="f3ed7-123">ETag des Windows IoT-Gerätediensts.</span><span class="sxs-lookup"><span data-stu-id="f3ed7-123">ETag of the Windows IoT Device Service.</span></span>
<span data-ttu-id="f3ed7-124">Geben Sie nicht an, dass ein neuer Windows IoT-Gerätedienst erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="f3ed7-124">Do not specify for creating a new Windows IoT Device Service.</span></span>
<span data-ttu-id="f3ed7-125">Erforderlich zum Aktualisieren eines vorhandenen Windows IoT-Gerätediensts.</span><span class="sxs-lookup"><span data-stu-id="f3ed7-125">Required to update an existing Windows IoT Device Service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3ed7-126">-Location</span><span class="sxs-lookup"><span data-stu-id="f3ed7-126">-Location</span></span>
<span data-ttu-id="f3ed7-127">Azure-Region, in der sich die Ressource lebt</span><span class="sxs-lookup"><span data-stu-id="f3ed7-127">The Azure Region where the resource lives</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3ed7-128">-Name</span><span class="sxs-lookup"><span data-stu-id="f3ed7-128">-Name</span></span>
<span data-ttu-id="f3ed7-129">Der Name des Windows IoT-Gerätediensts.</span><span class="sxs-lookup"><span data-stu-id="f3ed7-129">The name of the Windows IoT Device Service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3ed7-130">-Note</span><span class="sxs-lookup"><span data-stu-id="f3ed7-130">-Note</span></span>
<span data-ttu-id="f3ed7-131">Hinweise zum Windows IoT-Gerätedienst.</span><span class="sxs-lookup"><span data-stu-id="f3ed7-131">Windows IoT Device Service notes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3ed7-132">-Quantity</span><span class="sxs-lookup"><span data-stu-id="f3ed7-132">-Quantity</span></span>
<span data-ttu-id="f3ed7-133">Gerätezuordnung des Windows IoT-Gerätediensts,</span><span class="sxs-lookup"><span data-stu-id="f3ed7-133">Windows IoT Device Service device allocation,</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3ed7-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3ed7-134">-ResourceGroupName</span></span>
<span data-ttu-id="f3ed7-135">Der Name der Ressourcengruppe, die den Windows IoT-Gerätedienst enthält.</span><span class="sxs-lookup"><span data-stu-id="f3ed7-135">The name of the resource group that contains the Windows IoT Device Service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3ed7-136">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f3ed7-136">-SubscriptionId</span></span>
<span data-ttu-id="f3ed7-137">Die Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="f3ed7-137">The subscription identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3ed7-138">-Tag</span><span class="sxs-lookup"><span data-stu-id="f3ed7-138">-Tag</span></span>
<span data-ttu-id="f3ed7-139">Ressourcentags.</span><span class="sxs-lookup"><span data-stu-id="f3ed7-139">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3ed7-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f3ed7-140">-Confirm</span></span>
<span data-ttu-id="f3ed7-141">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f3ed7-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f3ed7-142">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="f3ed7-142">-WhatIf</span></span>
<span data-ttu-id="f3ed7-143">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f3ed7-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f3ed7-144">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f3ed7-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f3ed7-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3ed7-145">CommonParameters</span></span>
<span data-ttu-id="f3ed7-146">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3ed7-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3ed7-147">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f3ed7-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3ed7-148">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f3ed7-148">INPUTS</span></span>

## <span data-ttu-id="f3ed7-149">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f3ed7-149">OUTPUTS</span></span>

### <span data-ttu-id="f3ed7-150">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.Api20190601.IDeviceService</span><span class="sxs-lookup"><span data-stu-id="f3ed7-150">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.Api20190601.IDeviceService</span></span>

## <span data-ttu-id="f3ed7-151">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="f3ed7-151">NOTES</span></span>

<span data-ttu-id="f3ed7-152">ALIASE</span><span class="sxs-lookup"><span data-stu-id="f3ed7-152">ALIASES</span></span>

## <span data-ttu-id="f3ed7-153">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="f3ed7-153">RELATED LINKS</span></span>

