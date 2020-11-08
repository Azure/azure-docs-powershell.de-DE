---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/remove-aziotdeviceprovisioningserviceenrollment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceEnrollment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceEnrollment.md
ms.openlocfilehash: f8b16d95d582e29be6f49cac9eaeb00bcda67de0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94173815"
---
# <span data-ttu-id="f8fe7-101">Remove-AzIoTDeviceProvisioningServiceEnrollment</span><span class="sxs-lookup"><span data-stu-id="f8fe7-101">Remove-AzIoTDeviceProvisioningServiceEnrollment</span></span>

## <span data-ttu-id="f8fe7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f8fe7-102">SYNOPSIS</span></span>
<span data-ttu-id="f8fe7-103">Löschen eines Geräte Registrierungseintrags</span><span class="sxs-lookup"><span data-stu-id="f8fe7-103">Delete a device enrollment record.</span></span>

## <span data-ttu-id="f8fe7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f8fe7-104">SYNTAX</span></span>

### <span data-ttu-id="f8fe7-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="f8fe7-105">ResourceSet (Default)</span></span>
```
Remove-AzIoTDeviceProvisioningServiceEnrollment [-ResourceGroupName] <String> [-DpsName] <String>
 [-RegistrationId <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f8fe7-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="f8fe7-106">InputObjectSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceEnrollment [-DpsObject] <PSProvisioningServiceDescription>
 [-RegistrationId <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f8fe7-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="f8fe7-107">ResourceIdSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceEnrollment [-ResourceId] <String> [-RegistrationId <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f8fe7-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f8fe7-108">DESCRIPTION</span></span>
<span data-ttu-id="f8fe7-109">Löschen Sie eine Geräteregistrierung in einem Azure viel Hub-Device-Bereitstellungsdienst.</span><span class="sxs-lookup"><span data-stu-id="f8fe7-109">Delete a device enrollment in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="f8fe7-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f8fe7-110">EXAMPLES</span></span>

### <span data-ttu-id="f8fe7-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f8fe7-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -Passthru
```

<span data-ttu-id="f8fe7-112">Löschen eines angegebenen Registrierungseintrags</span><span class="sxs-lookup"><span data-stu-id="f8fe7-112">Delete a specified enrollment record.</span></span>

### <span data-ttu-id="f8fe7-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="f8fe7-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Passthru
```

<span data-ttu-id="f8fe7-114">Löschen Sie alle Registrierungseinträge.</span><span class="sxs-lookup"><span data-stu-id="f8fe7-114">Delete all enrollment records.</span></span>

## <span data-ttu-id="f8fe7-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="f8fe7-115">PARAMETERS</span></span>

### <span data-ttu-id="f8fe7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8fe7-116">-DefaultProfile</span></span>
<span data-ttu-id="f8fe7-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f8fe7-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f8fe7-118">-DpsName</span><span class="sxs-lookup"><span data-stu-id="f8fe7-118">-DpsName</span></span>
<span data-ttu-id="f8fe7-119">Name des viel Geräte Bereitstellungs Diensts</span><span class="sxs-lookup"><span data-stu-id="f8fe7-119">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="f8fe7-120">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="f8fe7-120">-DpsObject</span></span>
<span data-ttu-id="f8fe7-121">Viel Geräte Bereitstellungsdienst Objekt</span><span class="sxs-lookup"><span data-stu-id="f8fe7-121">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="f8fe7-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f8fe7-122">-PassThru</span></span>
<span data-ttu-id="f8fe7-123">Ermöglicht das Zurückgeben des booleschen Objekts.</span><span class="sxs-lookup"><span data-stu-id="f8fe7-123">Allows to return the boolean object.</span></span>
<span data-ttu-id="f8fe7-124">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="f8fe7-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="f8fe7-125">-Registrierungs-Nr</span><span class="sxs-lookup"><span data-stu-id="f8fe7-125">-RegistrationId</span></span>
<span data-ttu-id="f8fe7-126">Individuelle Registrierungs-ID für die Registrierung.</span><span class="sxs-lookup"><span data-stu-id="f8fe7-126">Individual enrollment registration id.</span></span>

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

### <span data-ttu-id="f8fe7-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8fe7-127">-ResourceGroupName</span></span>
<span data-ttu-id="f8fe7-128">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="f8fe7-128">Name of the Resource Group</span></span>

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

### <span data-ttu-id="f8fe7-129">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="f8fe7-129">-ResourceId</span></span>
<span data-ttu-id="f8fe7-130">Ressourcen-ID des Geräte Bereitstellungs Diensts</span><span class="sxs-lookup"><span data-stu-id="f8fe7-130">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="f8fe7-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f8fe7-131">-Confirm</span></span>
<span data-ttu-id="f8fe7-132">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f8fe7-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f8fe7-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f8fe7-133">-WhatIf</span></span>
<span data-ttu-id="f8fe7-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f8fe7-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f8fe7-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f8fe7-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f8fe7-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8fe7-136">CommonParameters</span></span>
<span data-ttu-id="f8fe7-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8fe7-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8fe7-138">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f8fe7-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8fe7-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f8fe7-139">INPUTS</span></span>

### <span data-ttu-id="f8fe7-140">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="f8fe7-140">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="f8fe7-141">System. String</span><span class="sxs-lookup"><span data-stu-id="f8fe7-141">System.String</span></span>

## <span data-ttu-id="f8fe7-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f8fe7-142">OUTPUTS</span></span>

### <span data-ttu-id="f8fe7-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f8fe7-143">System.Boolean</span></span>

## <span data-ttu-id="f8fe7-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="f8fe7-144">NOTES</span></span>

## <span data-ttu-id="f8fe7-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f8fe7-145">RELATED LINKS</span></span>
