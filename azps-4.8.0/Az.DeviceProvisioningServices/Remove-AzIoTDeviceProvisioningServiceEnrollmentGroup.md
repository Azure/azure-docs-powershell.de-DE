---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/remove-aziotdeviceprovisioningserviceenrollmentgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
ms.openlocfilehash: ce1fe3b50d8198dd9ee1965a3a3ab7a2409e1145
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94173820"
---
# <span data-ttu-id="920a4-101">Remove-AzIoTDeviceProvisioningServiceEnrollmentGroup</span><span class="sxs-lookup"><span data-stu-id="920a4-101">Remove-AzIoTDeviceProvisioningServiceEnrollmentGroup</span></span>

## <span data-ttu-id="920a4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="920a4-102">SYNOPSIS</span></span>
<span data-ttu-id="920a4-103">Löschen Sie eine Geräte Registrierungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="920a4-103">Delete a device enrollment group.</span></span>

## <span data-ttu-id="920a4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="920a4-104">SYNTAX</span></span>

### <span data-ttu-id="920a4-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="920a4-105">ResourceSet (Default)</span></span>
```
Remove-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceGroupName] <String> [-DpsName] <String>
 [-Name <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="920a4-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="920a4-106">InputObjectSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceEnrollmentGroup [-DpsObject] <PSProvisioningServiceDescription>
 [-Name <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="920a4-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="920a4-107">ResourceIdSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceId] <String> [-Name <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="920a4-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="920a4-108">DESCRIPTION</span></span>
<span data-ttu-id="920a4-109">Löschen Sie eine Registrierungsgruppe in einem Azure viel Hub-Device-Bereitstellungsdienst.</span><span class="sxs-lookup"><span data-stu-id="920a4-109">Delete an enrollment group in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="920a4-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="920a4-110">EXAMPLES</span></span>

### <span data-ttu-id="920a4-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="920a4-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Name "enroll1" -Passthru
```

<span data-ttu-id="920a4-112">Löschen einer angegebenen Registrierungsgruppe</span><span class="sxs-lookup"><span data-stu-id="920a4-112">Delete a specified enrollment group.</span></span>

### <span data-ttu-id="920a4-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="920a4-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Passthru
```

<span data-ttu-id="920a4-114">Löschen aller Registrierungs Gruppen</span><span class="sxs-lookup"><span data-stu-id="920a4-114">Delete all enrollment groups.</span></span>

## <span data-ttu-id="920a4-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="920a4-115">PARAMETERS</span></span>

### <span data-ttu-id="920a4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="920a4-116">-DefaultProfile</span></span>
<span data-ttu-id="920a4-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="920a4-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="920a4-118">-DpsName</span><span class="sxs-lookup"><span data-stu-id="920a4-118">-DpsName</span></span>
<span data-ttu-id="920a4-119">Name des viel Geräte Bereitstellungs Diensts</span><span class="sxs-lookup"><span data-stu-id="920a4-119">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="920a4-120">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="920a4-120">-DpsObject</span></span>
<span data-ttu-id="920a4-121">Viel Geräte Bereitstellungsdienst Objekt</span><span class="sxs-lookup"><span data-stu-id="920a4-121">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="920a4-122">-Name</span><span class="sxs-lookup"><span data-stu-id="920a4-122">-Name</span></span>
<span data-ttu-id="920a4-123">Der Name der Registrierungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="920a4-123">Name of the enrollment group.</span></span>

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

### <span data-ttu-id="920a4-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="920a4-124">-PassThru</span></span>
<span data-ttu-id="920a4-125">Ermöglicht das Zurückgeben des booleschen Objekts.</span><span class="sxs-lookup"><span data-stu-id="920a4-125">Allows to return the boolean object.</span></span>
<span data-ttu-id="920a4-126">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="920a4-126">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="920a4-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="920a4-127">-ResourceGroupName</span></span>
<span data-ttu-id="920a4-128">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="920a4-128">Name of the Resource Group</span></span>

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

### <span data-ttu-id="920a4-129">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="920a4-129">-ResourceId</span></span>
<span data-ttu-id="920a4-130">Ressourcen-ID des Geräte Bereitstellungs Diensts</span><span class="sxs-lookup"><span data-stu-id="920a4-130">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="920a4-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="920a4-131">-Confirm</span></span>
<span data-ttu-id="920a4-132">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="920a4-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="920a4-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="920a4-133">-WhatIf</span></span>
<span data-ttu-id="920a4-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="920a4-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="920a4-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="920a4-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="920a4-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="920a4-136">CommonParameters</span></span>
<span data-ttu-id="920a4-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="920a4-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="920a4-138">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="920a4-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="920a4-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="920a4-139">INPUTS</span></span>

### <span data-ttu-id="920a4-140">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="920a4-140">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="920a4-141">System. String</span><span class="sxs-lookup"><span data-stu-id="920a4-141">System.String</span></span>

## <span data-ttu-id="920a4-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="920a4-142">OUTPUTS</span></span>

### <span data-ttu-id="920a4-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="920a4-143">System.Boolean</span></span>

## <span data-ttu-id="920a4-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="920a4-144">NOTES</span></span>

## <span data-ttu-id="920a4-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="920a4-145">RELATED LINKS</span></span>
