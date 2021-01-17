---
external help file: ''
Module Name: Az.WindowsIotServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.windowsiotservices/get-azwindowsiotservicesdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/WindowsIotServices/help/Get-AzWindowsIotServicesDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/WindowsIotServices/help/Get-AzWindowsIotServicesDevice.md
ms.openlocfilehash: b9236dc7c3e4a12c9be6b72cd63874044ee49065
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98302635"
---
# <span data-ttu-id="496c4-101">Get-AzWindowsIotServicesDevice</span><span class="sxs-lookup"><span data-stu-id="496c4-101">Get-AzWindowsIotServicesDevice</span></span>

## <span data-ttu-id="496c4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="496c4-102">SYNOPSIS</span></span>
<span data-ttu-id="496c4-103">Sie erhalten die nicht sicherheitsbezogenen Metadaten eines Windows IoT-Gerätediensts.</span><span class="sxs-lookup"><span data-stu-id="496c4-103">Get the non-security related metadata of a Windows IoT Device Service.</span></span>

## <span data-ttu-id="496c4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="496c4-104">SYNTAX</span></span>

### <span data-ttu-id="496c4-105">Liste1 (Standard)</span><span class="sxs-lookup"><span data-stu-id="496c4-105">List1 (Default)</span></span>
```
Get-AzWindowsIotServicesDevice [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="496c4-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="496c4-106">Get</span></span>
```
Get-AzWindowsIotServicesDevice -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="496c4-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="496c4-107">GetViaIdentity</span></span>
```
Get-AzWindowsIotServicesDevice -InputObject <IWindowsIotServicesIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="496c4-108">Liste</span><span class="sxs-lookup"><span data-stu-id="496c4-108">List</span></span>
```
Get-AzWindowsIotServicesDevice -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="496c4-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="496c4-109">DESCRIPTION</span></span>
<span data-ttu-id="496c4-110">Sie erhalten die nicht sicherheitsbezogenen Metadaten eines Windows IoT-Gerätediensts.</span><span class="sxs-lookup"><span data-stu-id="496c4-110">Get the non-security related metadata of a Windows IoT Device Service.</span></span>

## <span data-ttu-id="496c4-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="496c4-111">EXAMPLES</span></span>

### <span data-ttu-id="496c4-112">Beispiel 1: Alle Windows -IoT-Dienste im Rahmen eines Abonnements erhalten</span><span class="sxs-lookup"><span data-stu-id="496c4-112">Example 1: Get all Windows IoT services under a subscription</span></span>
```powershell
PS C:\> Get-AzWindowsIotServicesDevice

Location Name    Type                                Etag
-------- ----    ----                                ----
West US  wsi-t01 Microsoft.WindowsIoT/DeviceServices "5c006e63-0000-0700-0000-5faa37830000"
eastus   wsi-t02 Microsoft.WindowsIoT/DeviceServices "5c006ad2-0000-0700-0000-5faa3e090000"
```

<span data-ttu-id="496c4-113">Dieser Befehl ruft alle Windows -IoT-Dienste unter einem Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="496c4-113">This command gets all Windows IoT services under a subscription.</span></span>

### <span data-ttu-id="496c4-114">Beispiel 2: Alle Windows -IoT-Dienste unter einer Ressourcengruppe erhalten</span><span class="sxs-lookup"><span data-stu-id="496c4-114">Example 2: Get all Windows IoT services under a resource group</span></span>
```powershell
PS C:\> Get-AzWindowsIotServicesDevice -ResourceGroupName azure-rg-test

Location Name    Type                                Etag
-------- ----    ----                                ----
West US  wsi-t01 Microsoft.WindowsIoT/DeviceServices "5c006e63-0000-0700-0000-5faa37830000"
eastus   wsi-t02 Microsoft.WindowsIoT/DeviceServices "5c006ad2-0000-0700-0000-5faa3e090000"
```

<span data-ttu-id="496c4-115">Dieser Befehl ruft alle Windows -IoT-Dienste unter einer Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="496c4-115">This command gets all Windows IoT services under a resource group.</span></span>

### <span data-ttu-id="496c4-116">Beispiel 3: Erhalten eines Windows -IoT-Diensts nach Name</span><span class="sxs-lookup"><span data-stu-id="496c4-116">Example 3: Get a Windows IoT service by name</span></span>
```powershell
PS C:\> Get-AzWindowsIotServicesDevice -ResourceGroupName azure-rg-test -Name wsi-t01

Location Name    Type                                Etag
-------- ----    ----                                ----
West US  wsi-t01 Microsoft.WindowsIoT/DeviceServices "5c006e63-0000-0700-0000-5faa37830000"
```

<span data-ttu-id="496c4-117">Dieser Befehl ruft einen Windows -IoT-Dienst nach Name ab.</span><span class="sxs-lookup"><span data-stu-id="496c4-117">This command gets a Windows IoT service by name.</span></span>

### <span data-ttu-id="496c4-118">Beispiel 4: Erhalten eines Windows -IoT-Diensts nach Objekt</span><span class="sxs-lookup"><span data-stu-id="496c4-118">Example 4: Get a Windows IoT service by object</span></span>
```powershell
PS C:\> $wsi = New-AzWindowsIotServicesDevice -Name wsi-t01 -ResourceGroupName azure-rg-test -Location eastus -Quantity 10 -BillingDomainName 'microsoft.onmicrosoft.com' -AdminDomainName 'microsoft.onmicrosoft.com'
PS C:\> Get-AzWindowsIotServicesDevice -InputObject $wsi

Location Name    Type                                Etag
-------- ----    ----                                ----
West US  wsi-t01 Microsoft.WindowsIoT/DeviceServices "5c006e63-0000-0700-0000-5faa37830000"
```

<span data-ttu-id="496c4-119">Dieser Befehl ruft einen Windows -IoT-Dienst nach Objekt ab.</span><span class="sxs-lookup"><span data-stu-id="496c4-119">This command gets a Windows IoT service by object.</span></span>

### <span data-ttu-id="496c4-120">Beispiel 4: Erhalten eines Windows -IoT-Diensts per Pipeline</span><span class="sxs-lookup"><span data-stu-id="496c4-120">Example 4: Get a Windows IoT service by pipeline</span></span>
```powershell
PS C:\> $wsi = New-AzWindowsIotServicesDevice -Name wsi-t01 -ResourceGroupName azure-rg-test -Location eastus -Quantity 10 -BillingDomainName 'microsoft.onmicrosoft.com' -AdminDomainName 'microsoft.onmicrosoft.com' | Get-AzWindowsIotServicesDevice

Location Name    Type                                Etag
-------- ----    ----                                ----
West US  wsi-t01 Microsoft.WindowsIoT/DeviceServices "5c006e63-0000-0700-0000-5faa37830000"
```

<span data-ttu-id="496c4-121">Dieser Befehl ruft einen Windows -IoT-Dienst per Pipeline ab.</span><span class="sxs-lookup"><span data-stu-id="496c4-121">This command gets a Windows IoT service by pipeline.</span></span>

## <span data-ttu-id="496c4-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="496c4-122">PARAMETERS</span></span>

### <span data-ttu-id="496c4-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="496c4-123">-DefaultProfile</span></span>
<span data-ttu-id="496c4-124">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="496c4-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="496c4-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="496c4-125">-InputObject</span></span>
<span data-ttu-id="496c4-126">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="496c4-126">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.IWindowsIotServicesIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="496c4-127">-Name</span><span class="sxs-lookup"><span data-stu-id="496c4-127">-Name</span></span>
<span data-ttu-id="496c4-128">Der Name des Windows IoT-Gerätediensts.</span><span class="sxs-lookup"><span data-stu-id="496c4-128">The name of the Windows IoT Device Service.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="496c4-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="496c4-129">-ResourceGroupName</span></span>
<span data-ttu-id="496c4-130">Der Name der Ressourcengruppe, die den Windows IoT-Gerätedienst enthält.</span><span class="sxs-lookup"><span data-stu-id="496c4-130">The name of the resource group that contains the Windows IoT Device Service.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="496c4-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="496c4-131">-SubscriptionId</span></span>
<span data-ttu-id="496c4-132">Die Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="496c4-132">The subscription identifier.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="496c4-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="496c4-133">CommonParameters</span></span>
<span data-ttu-id="496c4-134">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="496c4-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="496c4-135">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="496c4-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="496c4-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="496c4-136">INPUTS</span></span>

### <span data-ttu-id="496c4-137">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.IWindowsIotServicesIdentity</span><span class="sxs-lookup"><span data-stu-id="496c4-137">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.IWindowsIotServicesIdentity</span></span>

## <span data-ttu-id="496c4-138">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="496c4-138">OUTPUTS</span></span>

### <span data-ttu-id="496c4-139">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.Api20190601.IDeviceService</span><span class="sxs-lookup"><span data-stu-id="496c4-139">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.Api20190601.IDeviceService</span></span>

## <span data-ttu-id="496c4-140">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="496c4-140">NOTES</span></span>

<span data-ttu-id="496c4-141">ALIASE</span><span class="sxs-lookup"><span data-stu-id="496c4-141">ALIASES</span></span>

<span data-ttu-id="496c4-142">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="496c4-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="496c4-143">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="496c4-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="496c4-144">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="496c4-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="496c4-145">INPUTOBJECT <IWindowsIotServicesIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="496c4-145">INPUTOBJECT <IWindowsIotServicesIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="496c4-146">`[DeviceName <String>]`: Der Name des Windows IoT-Gerätediensts.</span><span class="sxs-lookup"><span data-stu-id="496c4-146">`[DeviceName <String>]`: The name of the Windows IoT Device Service.</span></span>
  - <span data-ttu-id="496c4-147">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="496c4-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="496c4-148">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die den Windows IoT-Gerätedienst enthält.</span><span class="sxs-lookup"><span data-stu-id="496c4-148">`[ResourceGroupName <String>]`: The name of the resource group that contains the Windows IoT Device Service.</span></span>
  - <span data-ttu-id="496c4-149">`[SubscriptionId <String>]`: Die Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="496c4-149">`[SubscriptionId <String>]`: The subscription identifier.</span></span>

## <span data-ttu-id="496c4-150">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="496c4-150">RELATED LINKS</span></span>

