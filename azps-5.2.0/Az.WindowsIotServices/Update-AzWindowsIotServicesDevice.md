---
external help file: ''
Module Name: Az.WindowsIotServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.windowsiotservices/update-azwindowsiotservicesdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/WindowsIotServices/help/Update-AzWindowsIotServicesDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/WindowsIotServices/help/Update-AzWindowsIotServicesDevice.md
ms.openlocfilehash: 5e50ad3dc1ce2396dfb7a2b498efc82c4e95e430
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98371466"
---
# <span data-ttu-id="3b28a-101">Update-AzWindowsIotServicesDevice</span><span class="sxs-lookup"><span data-stu-id="3b28a-101">Update-AzWindowsIotServicesDevice</span></span>

## <span data-ttu-id="3b28a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3b28a-102">SYNOPSIS</span></span>
<span data-ttu-id="3b28a-103">Aktualisiert die Metadaten eines Windows IoT-Gerätediensts.</span><span class="sxs-lookup"><span data-stu-id="3b28a-103">Updates the metadata of a Windows IoT Device Service.</span></span>
<span data-ttu-id="3b28a-104">Das übliche Muster zum Ändern einer Eigenschaft besteht im Abrufen der Windows IoT-Gerätedienstmetadaten und Sicherheitsmetadaten, die dann mit den geänderten Werten in einem neuen Textkörper kombiniert werden, um den Windows IoT-Gerätedienst zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="3b28a-104">The usual pattern to modify a property is to retrieve the Windows IoT Device Service metadata and security metadata, and then combine them with the modified values in a new body to update the Windows IoT Device Service.</span></span>

## <span data-ttu-id="3b28a-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3b28a-105">SYNTAX</span></span>

### <span data-ttu-id="3b28a-106">UpdateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="3b28a-106">UpdateExpanded (Default)</span></span>
```
Update-AzWindowsIotServicesDevice -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-IfMatch <String>] [-AdminDomainName <String>] [-BillingDomainName <String>] [-Etag <String>]
 [-Location <String>] [-Note <String>] [-Quantity <Int64>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="3b28a-107">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="3b28a-107">UpdateViaIdentityExpanded</span></span>
```
Update-AzWindowsIotServicesDevice -InputObject <IWindowsIotServicesIdentity> [-IfMatch <String>]
 [-AdminDomainName <String>] [-BillingDomainName <String>] [-Etag <String>] [-Location <String>]
 [-Note <String>] [-Quantity <Int64>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="3b28a-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3b28a-108">DESCRIPTION</span></span>
<span data-ttu-id="3b28a-109">Aktualisiert die Metadaten eines Windows IoT-Gerätediensts.</span><span class="sxs-lookup"><span data-stu-id="3b28a-109">Updates the metadata of a Windows IoT Device Service.</span></span>
<span data-ttu-id="3b28a-110">Das übliche Muster zum Ändern einer Eigenschaft besteht im Abrufen der Windows IoT-Gerätedienstmetadaten und Sicherheitsmetadaten, die dann mit den geänderten Werten in einem neuen Textkörper kombiniert werden, um den Windows IoT-Gerätedienst zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="3b28a-110">The usual pattern to modify a property is to retrieve the Windows IoT Device Service metadata and security metadata, and then combine them with the modified values in a new body to update the Windows IoT Device Service.</span></span>

## <span data-ttu-id="3b28a-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="3b28a-111">EXAMPLES</span></span>

### <span data-ttu-id="3b28a-112">Beispiel 1: Aktualisieren eines Windows -IoT-Diensts nach Name</span><span class="sxs-lookup"><span data-stu-id="3b28a-112">Example 1: Update a Windows IoT services by name</span></span>
```powershell
PS C:\> Update-AzWindowsIotServicesDevice -Name wsi-t03 -ResourceGroupName azure-rg-test -Quantity 10

Location Name    Type                                Etag
-------- ----    ----                                ----
eastus   wsi-t03 Microsoft.WindowsIoT/DeviceServices "5d006a5c-0000-0700-0000-5faa46760000"
```

<span data-ttu-id="3b28a-113">Mit diesem Befehl werden Windows -IoT-Dienste nach Name aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="3b28a-113">This command updates a Windows IoT services by name.</span></span>

### <span data-ttu-id="3b28a-114">Beispiel 2: Aktualisieren eines Windows -IoT-Diensts per Pipeline</span><span class="sxs-lookup"><span data-stu-id="3b28a-114">Example 2: Update a Windows IoT services by pipeline</span></span>
```powershell
PS C:\> Get-AzWindowsIotServicesDevice -Name wsi-t03 -ResourceGroupName azure-rg-test | Update-AzWindowsIotServicesDevice-Quantity 100 -Tag @{'oper'='update'}

Location Name    Type                                Etag
-------- ----    ----                                ----
West US  wsi-t01 Microsoft.WindowsIoT/DeviceServices "5d005f5f-0000-0700-0000-5faa46ae0000"
```

<span data-ttu-id="3b28a-115">Mit diesem Befehl werden Windows -IoT-Dienste per Pipeline aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="3b28a-115">This command updates a Windows IoT services by pipeline.</span></span>

## <span data-ttu-id="3b28a-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3b28a-116">PARAMETERS</span></span>

### <span data-ttu-id="3b28a-117">-AdminDomainName</span><span class="sxs-lookup"><span data-stu-id="3b28a-117">-AdminDomainName</span></span>
<span data-ttu-id="3b28a-118">Oem-AAD-Domäne des Windows IoT-Gerätediensts</span><span class="sxs-lookup"><span data-stu-id="3b28a-118">Windows IoT Device Service OEM AAD domain</span></span>

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

### <span data-ttu-id="3b28a-119">-BillingDomainName</span><span class="sxs-lookup"><span data-stu-id="3b28a-119">-BillingDomainName</span></span>
<span data-ttu-id="3b28a-120">Windows IoT Device Service ODM AAD domain</span><span class="sxs-lookup"><span data-stu-id="3b28a-120">Windows IoT Device Service ODM AAD domain</span></span>

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

### <span data-ttu-id="3b28a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b28a-121">-DefaultProfile</span></span>
<span data-ttu-id="3b28a-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3b28a-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3b28a-123">-Etag</span><span class="sxs-lookup"><span data-stu-id="3b28a-123">-Etag</span></span>
<span data-ttu-id="3b28a-124">Das #A0 ist *nicht* erforderlich.</span><span class="sxs-lookup"><span data-stu-id="3b28a-124">The Etag field is *not* required.</span></span>
<span data-ttu-id="3b28a-125">Wenn sie im Antworttext bereitgestellt wird, muss sie auch als Kopfzeile nach der normalen #A0 bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="3b28a-125">If it is provided in the response body, it must also be provided as a header per the normal ETag convention.</span></span>

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

### <span data-ttu-id="3b28a-126">-IfMatch</span><span class="sxs-lookup"><span data-stu-id="3b28a-126">-IfMatch</span></span>
<span data-ttu-id="3b28a-127">ETag des Windows IoT-Gerätediensts.</span><span class="sxs-lookup"><span data-stu-id="3b28a-127">ETag of the Windows IoT Device Service.</span></span>
<span data-ttu-id="3b28a-128">Geben Sie nicht an, dass ein völlig neuer Windows IoT-Gerätedienst erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="3b28a-128">Do not specify for creating a brand new Windows IoT Device Service.</span></span>
<span data-ttu-id="3b28a-129">Erforderlich zum Aktualisieren eines vorhandenen Windows IoT-Gerätediensts.</span><span class="sxs-lookup"><span data-stu-id="3b28a-129">Required to update an existing Windows IoT Device Service.</span></span>

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

### <span data-ttu-id="3b28a-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3b28a-130">-InputObject</span></span>
<span data-ttu-id="3b28a-131">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="3b28a-131">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.IWindowsIotServicesIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3b28a-132">-Location</span><span class="sxs-lookup"><span data-stu-id="3b28a-132">-Location</span></span>
<span data-ttu-id="3b28a-133">Azure-Region, in der sich die Ressource lebt</span><span class="sxs-lookup"><span data-stu-id="3b28a-133">The Azure Region where the resource lives</span></span>

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

### <span data-ttu-id="3b28a-134">-Name</span><span class="sxs-lookup"><span data-stu-id="3b28a-134">-Name</span></span>
<span data-ttu-id="3b28a-135">Der Name des Windows IoT-Gerätediensts.</span><span class="sxs-lookup"><span data-stu-id="3b28a-135">The name of the Windows IoT Device Service.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b28a-136">-Note</span><span class="sxs-lookup"><span data-stu-id="3b28a-136">-Note</span></span>
<span data-ttu-id="3b28a-137">Hinweise zum Windows IoT-Gerätedienst.</span><span class="sxs-lookup"><span data-stu-id="3b28a-137">Windows IoT Device Service notes.</span></span>

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

### <span data-ttu-id="3b28a-138">-Quantity</span><span class="sxs-lookup"><span data-stu-id="3b28a-138">-Quantity</span></span>
<span data-ttu-id="3b28a-139">Gerätezuordnung des Windows IoT-Gerätediensts,</span><span class="sxs-lookup"><span data-stu-id="3b28a-139">Windows IoT Device Service device allocation,</span></span>

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

### <span data-ttu-id="3b28a-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b28a-140">-ResourceGroupName</span></span>
<span data-ttu-id="3b28a-141">Der Name der Ressourcengruppe, die den Windows IoT-Gerätedienst enthält.</span><span class="sxs-lookup"><span data-stu-id="3b28a-141">The name of the resource group that contains the Windows IoT Device Service.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b28a-142">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3b28a-142">-SubscriptionId</span></span>
<span data-ttu-id="3b28a-143">Die Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="3b28a-143">The subscription identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b28a-144">-Tag</span><span class="sxs-lookup"><span data-stu-id="3b28a-144">-Tag</span></span>
<span data-ttu-id="3b28a-145">Ressourcentags.</span><span class="sxs-lookup"><span data-stu-id="3b28a-145">Resource tags.</span></span>

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

### <span data-ttu-id="3b28a-146">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3b28a-146">-Confirm</span></span>
<span data-ttu-id="3b28a-147">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3b28a-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3b28a-148">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="3b28a-148">-WhatIf</span></span>
<span data-ttu-id="3b28a-149">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3b28a-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3b28a-150">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3b28a-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3b28a-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b28a-151">CommonParameters</span></span>
<span data-ttu-id="3b28a-152">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b28a-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b28a-153">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3b28a-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b28a-154">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="3b28a-154">INPUTS</span></span>

### <span data-ttu-id="3b28a-155">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.IWindowsIotServicesIdentity</span><span class="sxs-lookup"><span data-stu-id="3b28a-155">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.IWindowsIotServicesIdentity</span></span>

## <span data-ttu-id="3b28a-156">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="3b28a-156">OUTPUTS</span></span>

### <span data-ttu-id="3b28a-157">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.Api20190601.IDeviceService</span><span class="sxs-lookup"><span data-stu-id="3b28a-157">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.Api20190601.IDeviceService</span></span>

## <span data-ttu-id="3b28a-158">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="3b28a-158">NOTES</span></span>

<span data-ttu-id="3b28a-159">ALIASE</span><span class="sxs-lookup"><span data-stu-id="3b28a-159">ALIASES</span></span>

<span data-ttu-id="3b28a-160">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="3b28a-160">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="3b28a-161">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="3b28a-161">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3b28a-162">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="3b28a-162">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="3b28a-163">INPUTOBJECT <IWindowsIotServicesIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="3b28a-163">INPUTOBJECT <IWindowsIotServicesIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="3b28a-164">`[DeviceName <String>]`: Der Name des Windows IoT-Gerätediensts.</span><span class="sxs-lookup"><span data-stu-id="3b28a-164">`[DeviceName <String>]`: The name of the Windows IoT Device Service.</span></span>
  - <span data-ttu-id="3b28a-165">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="3b28a-165">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="3b28a-166">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die den Windows IoT-Gerätedienst enthält.</span><span class="sxs-lookup"><span data-stu-id="3b28a-166">`[ResourceGroupName <String>]`: The name of the resource group that contains the Windows IoT Device Service.</span></span>
  - <span data-ttu-id="3b28a-167">`[SubscriptionId <String>]`: Die Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="3b28a-167">`[SubscriptionId <String>]`: The subscription identifier.</span></span>

## <span data-ttu-id="3b28a-168">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="3b28a-168">RELATED LINKS</span></span>

