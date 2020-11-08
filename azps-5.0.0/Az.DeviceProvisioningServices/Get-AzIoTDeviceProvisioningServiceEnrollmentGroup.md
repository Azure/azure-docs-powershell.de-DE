---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/get-aziotdeviceprovisioningserviceenrollmentgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
ms.openlocfilehash: f4cac1380a6ed089d3b3e7b368eb15486e4c12d4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94175721"
---
# <span data-ttu-id="f4da4-101">Get-AzIoTDeviceProvisioningServiceEnrollmentGroup</span><span class="sxs-lookup"><span data-stu-id="f4da4-101">Get-AzIoTDeviceProvisioningServiceEnrollmentGroup</span></span>

## <span data-ttu-id="f4da4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f4da4-102">SYNOPSIS</span></span>
<span data-ttu-id="f4da4-103">Rufen Sie eine Geräte Registrierungsgruppe ab.</span><span class="sxs-lookup"><span data-stu-id="f4da4-103">Get a device enrollment group.</span></span>

## <span data-ttu-id="f4da4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f4da4-104">SYNTAX</span></span>

### <span data-ttu-id="f4da4-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="f4da4-105">ResourceSet (Default)</span></span>
```
Get-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceGroupName] <String> [-DpsName] <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f4da4-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="f4da4-106">InputObjectSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceEnrollmentGroup [-DpsObject] <PSProvisioningServiceDescription>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f4da4-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="f4da4-107">ResourceIdSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f4da4-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f4da4-108">DESCRIPTION</span></span>
<span data-ttu-id="f4da4-109">Rufen Sie die Details einer Registrierungsgruppe ab, oder Listen Sie alle Registrierungs Gruppen in einem Azure-to-Bereitstellungsdienst für Hub-Geräte auf.</span><span class="sxs-lookup"><span data-stu-id="f4da4-109">Get the details of an enrollment group or list all enrollment groups in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="f4da4-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f4da4-110">EXAMPLES</span></span>

### <span data-ttu-id="f4da4-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f4da4-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Name "enroll1"
```

<span data-ttu-id="f4da4-112">Rufen Sie die Geräte Registrierungsgruppe in einem Azure viel-Bereitstellungsdienst für Hub-Devices ab.</span><span class="sxs-lookup"><span data-stu-id="f4da4-112">Get device enrollment group in an Azure IoT Hub Device Provisioning Service.</span></span>

### <span data-ttu-id="f4da4-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="f4da4-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps"
```

<span data-ttu-id="f4da4-114">Auflisten aller Geräte Registrierungs Gruppen in einem Azure viel Hub-Device-Bereitstellungsdienst</span><span class="sxs-lookup"><span data-stu-id="f4da4-114">List all device enrollment groups in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="f4da4-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="f4da4-115">PARAMETERS</span></span>

### <span data-ttu-id="f4da4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4da4-116">-DefaultProfile</span></span>
<span data-ttu-id="f4da4-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f4da4-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f4da4-118">-DpsName</span><span class="sxs-lookup"><span data-stu-id="f4da4-118">-DpsName</span></span>
<span data-ttu-id="f4da4-119">Name des viel Geräte Bereitstellungs Diensts</span><span class="sxs-lookup"><span data-stu-id="f4da4-119">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="f4da4-120">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="f4da4-120">-DpsObject</span></span>
<span data-ttu-id="f4da4-121">Viel Geräte Bereitstellungsdienst Objekt</span><span class="sxs-lookup"><span data-stu-id="f4da4-121">IoT Device Provisioning Service Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f4da4-122">-Name</span><span class="sxs-lookup"><span data-stu-id="f4da4-122">-Name</span></span>
<span data-ttu-id="f4da4-123">Der Name der Registrierungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="f4da4-123">Name of the enrollment group.</span></span>

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

### <span data-ttu-id="f4da4-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4da4-124">-ResourceGroupName</span></span>
<span data-ttu-id="f4da4-125">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="f4da4-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="f4da4-126">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="f4da4-126">-ResourceId</span></span>
<span data-ttu-id="f4da4-127">Ressourcen-ID des Geräte Bereitstellungs Diensts</span><span class="sxs-lookup"><span data-stu-id="f4da4-127">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="f4da4-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4da4-128">CommonParameters</span></span>
<span data-ttu-id="f4da4-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4da4-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4da4-130">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4da4-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4da4-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f4da4-131">INPUTS</span></span>

### <span data-ttu-id="f4da4-132">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="f4da4-132">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="f4da4-133">System. String</span><span class="sxs-lookup"><span data-stu-id="f4da4-133">System.String</span></span>

## <span data-ttu-id="f4da4-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f4da4-134">OUTPUTS</span></span>

### <span data-ttu-id="f4da4-135">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSEnrollmentGroup</span><span class="sxs-lookup"><span data-stu-id="f4da4-135">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSEnrollmentGroup</span></span>

### <span data-ttu-id="f4da4-136">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSEnrollmentGroups []</span><span class="sxs-lookup"><span data-stu-id="f4da4-136">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSEnrollmentGroups[]</span></span>

## <span data-ttu-id="f4da4-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="f4da4-137">NOTES</span></span>

## <span data-ttu-id="f4da4-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f4da4-138">RELATED LINKS</span></span>
