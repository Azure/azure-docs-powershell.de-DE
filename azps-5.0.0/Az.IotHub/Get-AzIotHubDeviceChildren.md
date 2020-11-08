---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubdevicechildren
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceChildren.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceChildren.md
ms.openlocfilehash: 1bc45aa06db70aff6eaec8eb1ff20b12318bb7e2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94177960"
---
# <span data-ttu-id="3efe3-101">Get-AzIotHubDeviceChildren</span><span class="sxs-lookup"><span data-stu-id="3efe3-101">Get-AzIotHubDeviceChildren</span></span>

## <span data-ttu-id="3efe3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3efe3-102">SYNOPSIS</span></span>
<span data-ttu-id="3efe3-103">Drucken Sie eine durch trennzeichengetrennte Liste der zugewiesenen untergeordneten Geräte.</span><span class="sxs-lookup"><span data-stu-id="3efe3-103">Print comma-separated list of assigned child devices.</span></span>

## <span data-ttu-id="3efe3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3efe3-104">SYNTAX</span></span>

### <span data-ttu-id="3efe3-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="3efe3-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubDeviceChildren [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3efe3-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="3efe3-106">InputObjectSet</span></span>
```
Get-AzIotHubDeviceChildren [-InputObject] <PSIotHub> [-DeviceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3efe3-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="3efe3-107">ResourceIdSet</span></span>
```
Get-AzIotHubDeviceChildren [-ResourceId] <String> [-DeviceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3efe3-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3efe3-108">DESCRIPTION</span></span>
<span data-ttu-id="3efe3-109">Alle zugewiesenen nicht-Edge-Geräte als durch trennzeichengetrennte Liste aller Edge-Geräte oder des angegebenen Geräts anzeigen.</span><span class="sxs-lookup"><span data-stu-id="3efe3-109">Show all assigned non-edge devices as comma-separated list of all edge devices or specified device.</span></span>

## <span data-ttu-id="3efe3-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3efe3-110">EXAMPLES</span></span>

### <span data-ttu-id="3efe3-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="3efe3-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubDeviceChildren -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1"

DeviceId  ChildrenDeviceId
--------  ----------------
myDevice1 {device1, device2}
```

<span data-ttu-id="3efe3-112">Alle zugewiesenen nicht-Edge-Geräte als durch trennzeichengetrennte Liste anzeigen.</span><span class="sxs-lookup"><span data-stu-id="3efe3-112">Show all assigned non-edge devices as comma-separated list.</span></span>

### <span data-ttu-id="3efe3-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="3efe3-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIotHubDeviceChildren -ResourceGroupName "myresourcegroup" -IotHubName "myiothub"

DeviceId  ChildrenDeviceId
--------  ----------------
myDevice1 {device1, device2}
myDevice2 {device3, device4, device5}
```

<span data-ttu-id="3efe3-114">Alle zugewiesenen nicht-Edge-Geräte als durch trennzeichengetrennte Liste aller edgegeräte anzeigen.</span><span class="sxs-lookup"><span data-stu-id="3efe3-114">Show all assigned non-edge devices as comma-separated list of all edge devices.</span></span>

## <span data-ttu-id="3efe3-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="3efe3-115">PARAMETERS</span></span>

### <span data-ttu-id="3efe3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3efe3-116">-DefaultProfile</span></span>
<span data-ttu-id="3efe3-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3efe3-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3efe3-118">-Geräte-Nr</span><span class="sxs-lookup"><span data-stu-id="3efe3-118">-DeviceId</span></span>
<span data-ttu-id="3efe3-119">Die ID des Edge-Geräts.</span><span class="sxs-lookup"><span data-stu-id="3efe3-119">Id of edge device.</span></span>

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

### <span data-ttu-id="3efe3-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="3efe3-120">-InputObject</span></span>
<span data-ttu-id="3efe3-121">IotHub-Objekt</span><span class="sxs-lookup"><span data-stu-id="3efe3-121">IotHub object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3efe3-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="3efe3-122">-IotHubName</span></span>
<span data-ttu-id="3efe3-123">Name des viel-Hubs</span><span class="sxs-lookup"><span data-stu-id="3efe3-123">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3efe3-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3efe3-124">-ResourceGroupName</span></span>
<span data-ttu-id="3efe3-125">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="3efe3-125">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3efe3-126">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="3efe3-126">-ResourceId</span></span>
<span data-ttu-id="3efe3-127">IotHub-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="3efe3-127">IotHub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3efe3-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3efe3-128">CommonParameters</span></span>
<span data-ttu-id="3efe3-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3efe3-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3efe3-130">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3efe3-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3efe3-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3efe3-131">INPUTS</span></span>

### <span data-ttu-id="3efe3-132">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="3efe3-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="3efe3-133">System. String</span><span class="sxs-lookup"><span data-stu-id="3efe3-133">System.String</span></span>

## <span data-ttu-id="3efe3-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3efe3-134">OUTPUTS</span></span>

### <span data-ttu-id="3efe3-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceChildren</span><span class="sxs-lookup"><span data-stu-id="3efe3-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceChildren</span></span>

### <span data-ttu-id="3efe3-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevicesChildren []</span><span class="sxs-lookup"><span data-stu-id="3efe3-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevicesChildren[]</span></span>

## <span data-ttu-id="3efe3-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="3efe3-137">NOTES</span></span>

## <span data-ttu-id="3efe3-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3efe3-138">RELATED LINKS</span></span>
