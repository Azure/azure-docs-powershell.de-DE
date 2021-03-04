---
external help file: ''
Module Name: Az.WindowsIotServices
online version: https://docs.microsoft.com/powershell/module/az.windowsiotservices/get-azwindowsiotservicesdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/WindowsIotServices/help/Get-AzWindowsIotServicesDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/WindowsIotServices/help/Get-AzWindowsIotServicesDevice.md
ms.openlocfilehash: 51e828245c62ddfcbaa925b3a22a916fd9148ada
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101948080"
---
# <span data-ttu-id="7b57a-101">Get-AzWindowsIotServicesDevice</span><span class="sxs-lookup"><span data-stu-id="7b57a-101">Get-AzWindowsIotServicesDevice</span></span>

## <span data-ttu-id="7b57a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7b57a-102">SYNOPSIS</span></span>
<span data-ttu-id="7b57a-103">Holen Sie sich die nicht sicherheitsbezogenen Metadaten eines Windows IoT-Gerätediensts.</span><span class="sxs-lookup"><span data-stu-id="7b57a-103">Get the non-security related metadata of a Windows IoT Device Service.</span></span>

## <span data-ttu-id="7b57a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7b57a-104">SYNTAX</span></span>

### <span data-ttu-id="7b57a-105">List1 (Standard)</span><span class="sxs-lookup"><span data-stu-id="7b57a-105">List1 (Default)</span></span>
```
Get-AzWindowsIotServicesDevice [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="7b57a-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="7b57a-106">Get</span></span>
```
Get-AzWindowsIotServicesDevice -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="7b57a-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="7b57a-107">GetViaIdentity</span></span>
```
Get-AzWindowsIotServicesDevice -InputObject <IWindowsIotServicesIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="7b57a-108">Liste</span><span class="sxs-lookup"><span data-stu-id="7b57a-108">List</span></span>
```
Get-AzWindowsIotServicesDevice -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="7b57a-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7b57a-109">DESCRIPTION</span></span>
<span data-ttu-id="7b57a-110">Holen Sie sich die nicht sicherheitsbezogenen Metadaten eines Windows IoT-Gerätediensts.</span><span class="sxs-lookup"><span data-stu-id="7b57a-110">Get the non-security related metadata of a Windows IoT Device Service.</span></span>

## <span data-ttu-id="7b57a-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="7b57a-111">EXAMPLES</span></span>

### <span data-ttu-id="7b57a-112">Beispiel 1: Alle Windows IoT-Dienste unter einem Abonnement erhalten</span><span class="sxs-lookup"><span data-stu-id="7b57a-112">Example 1: Get all Windows IoT services under a subscription</span></span>
```powershell
PS C:\> Get-AzWindowsIotServicesDevice

Location Name    Type                                Etag
-------- ----    ----                                ----
West US  wsi-t01 Microsoft.WindowsIoT/DeviceServices "5c006e63-0000-0700-0000-5faa37830000"
eastus   wsi-t02 Microsoft.WindowsIoT/DeviceServices "5c006ad2-0000-0700-0000-5faa3e090000"
```

<span data-ttu-id="7b57a-113">Dieser Befehl ruft alle Windows IoT-Dienste unter einem Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="7b57a-113">This command gets all Windows IoT services under a subscription.</span></span>

### <span data-ttu-id="7b57a-114">Beispiel 2: Alle Windows IoT-Dienste unter einer Ressourcengruppe erhalten</span><span class="sxs-lookup"><span data-stu-id="7b57a-114">Example 2: Get all Windows IoT services under a resource group</span></span>
```powershell
PS C:\> Get-AzWindowsIotServicesDevice -ResourceGroupName azure-rg-test

Location Name    Type                                Etag
-------- ----    ----                                ----
West US  wsi-t01 Microsoft.WindowsIoT/DeviceServices "5c006e63-0000-0700-0000-5faa37830000"
eastus   wsi-t02 Microsoft.WindowsIoT/DeviceServices "5c006ad2-0000-0700-0000-5faa3e090000"
```

<span data-ttu-id="7b57a-115">Dieser Befehl ruft alle Windows IoT-Dienste unter einer Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="7b57a-115">This command gets all Windows IoT services under a resource group.</span></span>

### <span data-ttu-id="7b57a-116">Beispiel 3: Erhalten eines Windows IoT-Diensts nach Name</span><span class="sxs-lookup"><span data-stu-id="7b57a-116">Example 3: Get a Windows IoT service by name</span></span>
```powershell
PS C:\> Get-AzWindowsIotServicesDevice -ResourceGroupName azure-rg-test -Name wsi-t01

Location Name    Type                                Etag
-------- ----    ----                                ----
West US  wsi-t01 Microsoft.WindowsIoT/DeviceServices "5c006e63-0000-0700-0000-5faa37830000"
```

<span data-ttu-id="7b57a-117">Dieser Befehl ruft einen Windows IoT-Dienst namens ab.</span><span class="sxs-lookup"><span data-stu-id="7b57a-117">This command gets a Windows IoT service by name.</span></span>

### <span data-ttu-id="7b57a-118">Beispiel 4: Erstellen eines Windows IoT-Diensts nach Objekt</span><span class="sxs-lookup"><span data-stu-id="7b57a-118">Example 4: Get a Windows IoT service by object</span></span>
```powershell
PS C:\> $wsi = New-AzWindowsIotServicesDevice -Name wsi-t01 -ResourceGroupName azure-rg-test -Location eastus -Quantity 10 -BillingDomainName 'microsoft.onmicrosoft.com' -AdminDomainName 'microsoft.onmicrosoft.com'
PS C:\> Get-AzWindowsIotServicesDevice -InputObject $wsi

Location Name    Type                                Etag
-------- ----    ----                                ----
West US  wsi-t01 Microsoft.WindowsIoT/DeviceServices "5c006e63-0000-0700-0000-5faa37830000"
```

<span data-ttu-id="7b57a-119">Dieser Befehl ruft einen Windows IoT-Dienst nach Objekt ab.</span><span class="sxs-lookup"><span data-stu-id="7b57a-119">This command gets a Windows IoT service by object.</span></span>

### <span data-ttu-id="7b57a-120">Beispiel 4: Einen Windows IoT-Dienst per Pipeline erhalten</span><span class="sxs-lookup"><span data-stu-id="7b57a-120">Example 4: Get a Windows IoT service by pipeline</span></span>
```powershell
PS C:\> $wsi = New-AzWindowsIotServicesDevice -Name wsi-t01 -ResourceGroupName azure-rg-test -Location eastus -Quantity 10 -BillingDomainName 'microsoft.onmicrosoft.com' -AdminDomainName 'microsoft.onmicrosoft.com' | Get-AzWindowsIotServicesDevice

Location Name    Type                                Etag
-------- ----    ----                                ----
West US  wsi-t01 Microsoft.WindowsIoT/DeviceServices "5c006e63-0000-0700-0000-5faa37830000"
```

<span data-ttu-id="7b57a-121">Dieser Befehl ruft einen Windows IoT-Dienst per Pipeline ab.</span><span class="sxs-lookup"><span data-stu-id="7b57a-121">This command gets a Windows IoT service by pipeline.</span></span>

## <span data-ttu-id="7b57a-122">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="7b57a-122">PARAMETERS</span></span>

### <span data-ttu-id="7b57a-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b57a-123">-DefaultProfile</span></span>
<span data-ttu-id="7b57a-124">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7b57a-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7b57a-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7b57a-125">-InputObject</span></span>
<span data-ttu-id="7b57a-126">Identitätsparameter Zum Erstellen lesen Sie den Abschnitt NOTIZEN für INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="7b57a-126">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="7b57a-127">-Name</span><span class="sxs-lookup"><span data-stu-id="7b57a-127">-Name</span></span>
<span data-ttu-id="7b57a-128">Der Name des Windows IoT-Gerätediensts.</span><span class="sxs-lookup"><span data-stu-id="7b57a-128">The name of the Windows IoT Device Service.</span></span>

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

### <span data-ttu-id="7b57a-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7b57a-129">-ResourceGroupName</span></span>
<span data-ttu-id="7b57a-130">Der Name der Ressourcengruppe, die den Windows IoT-Gerätedienst enthält.</span><span class="sxs-lookup"><span data-stu-id="7b57a-130">The name of the resource group that contains the Windows IoT Device Service.</span></span>

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

### <span data-ttu-id="7b57a-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7b57a-131">-SubscriptionId</span></span>
<span data-ttu-id="7b57a-132">Der Abonnementbezeichner.</span><span class="sxs-lookup"><span data-stu-id="7b57a-132">The subscription identifier.</span></span>

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

### <span data-ttu-id="7b57a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b57a-133">CommonParameters</span></span>
<span data-ttu-id="7b57a-134">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b57a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b57a-135">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7b57a-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b57a-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="7b57a-136">INPUTS</span></span>

### <span data-ttu-id="7b57a-137">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.IWindowsIotServicesIdentity</span><span class="sxs-lookup"><span data-stu-id="7b57a-137">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.IWindowsIotServicesIdentity</span></span>

## <span data-ttu-id="7b57a-138">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="7b57a-138">OUTPUTS</span></span>

### <span data-ttu-id="7b57a-139">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.Api20190601.IDeviceService</span><span class="sxs-lookup"><span data-stu-id="7b57a-139">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.Api20190601.IDeviceService</span></span>

## <span data-ttu-id="7b57a-140">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="7b57a-140">NOTES</span></span>

<span data-ttu-id="7b57a-141">ALIASE</span><span class="sxs-lookup"><span data-stu-id="7b57a-141">ALIASES</span></span>

<span data-ttu-id="7b57a-142">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="7b57a-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="7b57a-143">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="7b57a-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7b57a-144">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="7b57a-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="7b57a-145">INPUTOBJECT <IWindowsIotServicesIdentity> : Identitätsparameter</span><span class="sxs-lookup"><span data-stu-id="7b57a-145">INPUTOBJECT <IWindowsIotServicesIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="7b57a-146">`[DeviceName <String>]`: Der Name des Windows IoT-Gerätediensts.</span><span class="sxs-lookup"><span data-stu-id="7b57a-146">`[DeviceName <String>]`: The name of the Windows IoT Device Service.</span></span>
  - <span data-ttu-id="7b57a-147">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="7b57a-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="7b57a-148">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die den Windows IoT-Gerätedienst enthält.</span><span class="sxs-lookup"><span data-stu-id="7b57a-148">`[ResourceGroupName <String>]`: The name of the resource group that contains the Windows IoT Device Service.</span></span>
  - <span data-ttu-id="7b57a-149">`[SubscriptionId <String>]`: Der Abonnementbezeichner.</span><span class="sxs-lookup"><span data-stu-id="7b57a-149">`[SubscriptionId <String>]`: The subscription identifier.</span></span>

## <span data-ttu-id="7b57a-150">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="7b57a-150">RELATED LINKS</span></span>

