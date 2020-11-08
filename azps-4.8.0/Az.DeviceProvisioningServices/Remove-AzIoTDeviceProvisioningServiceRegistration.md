---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/remove-aziotdeviceprovisioningserviceregistration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceRegistration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceRegistration.md
ms.openlocfilehash: b0fa84887a54eb1f4e9c689c49fb08a1300cd62b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94173816"
---
# <span data-ttu-id="6caaa-101">Remove-AzIoTDeviceProvisioningServiceRegistration</span><span class="sxs-lookup"><span data-stu-id="6caaa-101">Remove-AzIoTDeviceProvisioningServiceRegistration</span></span>

## <span data-ttu-id="6caaa-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6caaa-102">SYNOPSIS</span></span>
<span data-ttu-id="6caaa-103">Löscht die Geräteregistrierung.</span><span class="sxs-lookup"><span data-stu-id="6caaa-103">Deletes the device registration.</span></span>

## <span data-ttu-id="6caaa-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6caaa-104">SYNTAX</span></span>

### <span data-ttu-id="6caaa-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="6caaa-105">ResourceSet (Default)</span></span>
```
Remove-AzIoTDeviceProvisioningServiceRegistration [-ResourceGroupName] <String> [-DpsName] <String>
 -RegistrationId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6caaa-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="6caaa-106">InputObjectSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceRegistration [-DpsObject] <PSProvisioningServiceDescription>
 -RegistrationId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6caaa-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="6caaa-107">ResourceIdSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceRegistration [-ResourceId] <String> -RegistrationId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6caaa-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6caaa-108">DESCRIPTION</span></span>
<span data-ttu-id="6caaa-109">Löschen Sie eine Geräteregistrierung in einem Azure viel Hub-Device-Bereitstellungsdienst.</span><span class="sxs-lookup"><span data-stu-id="6caaa-109">Delete a device registration in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="6caaa-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6caaa-110">EXAMPLES</span></span>

### <span data-ttu-id="6caaa-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="6caaa-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIoTDeviceProvisioningServiceRegistration -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -Passthru
```

<span data-ttu-id="6caaa-112">Löschen Sie eine Geräteregistrierung in einem Azure viel Hub-Device-Bereitstellungsdienst.</span><span class="sxs-lookup"><span data-stu-id="6caaa-112">Delete a device registration in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="6caaa-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="6caaa-113">PARAMETERS</span></span>

### <span data-ttu-id="6caaa-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6caaa-114">-DefaultProfile</span></span>
<span data-ttu-id="6caaa-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6caaa-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6caaa-116">-DpsName</span><span class="sxs-lookup"><span data-stu-id="6caaa-116">-DpsName</span></span>
<span data-ttu-id="6caaa-117">Name des viel Geräte Bereitstellungs Diensts</span><span class="sxs-lookup"><span data-stu-id="6caaa-117">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="6caaa-118">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="6caaa-118">-DpsObject</span></span>
<span data-ttu-id="6caaa-119">Viel Geräte Bereitstellungsdienst Objekt</span><span class="sxs-lookup"><span data-stu-id="6caaa-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="6caaa-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6caaa-120">-PassThru</span></span>
<span data-ttu-id="6caaa-121">Ermöglicht das Zurückgeben des booleschen Objekts.</span><span class="sxs-lookup"><span data-stu-id="6caaa-121">Allows to return the boolean object.</span></span>
<span data-ttu-id="6caaa-122">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="6caaa-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="6caaa-123">-Registrierungs-Nr</span><span class="sxs-lookup"><span data-stu-id="6caaa-123">-RegistrationId</span></span>
<span data-ttu-id="6caaa-124">Die ID der Geräteregistrierung.</span><span class="sxs-lookup"><span data-stu-id="6caaa-124">ID of device registration.</span></span>

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

### <span data-ttu-id="6caaa-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6caaa-125">-ResourceGroupName</span></span>
<span data-ttu-id="6caaa-126">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="6caaa-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="6caaa-127">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="6caaa-127">-ResourceId</span></span>
<span data-ttu-id="6caaa-128">Ressourcen-ID des Geräte Bereitstellungs Diensts</span><span class="sxs-lookup"><span data-stu-id="6caaa-128">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="6caaa-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="6caaa-129">-Confirm</span></span>
<span data-ttu-id="6caaa-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6caaa-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6caaa-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6caaa-131">-WhatIf</span></span>
<span data-ttu-id="6caaa-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6caaa-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6caaa-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6caaa-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6caaa-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6caaa-134">CommonParameters</span></span>
<span data-ttu-id="6caaa-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6caaa-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6caaa-136">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6caaa-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6caaa-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6caaa-137">INPUTS</span></span>

### <span data-ttu-id="6caaa-138">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="6caaa-138">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="6caaa-139">System. String</span><span class="sxs-lookup"><span data-stu-id="6caaa-139">System.String</span></span>

## <span data-ttu-id="6caaa-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6caaa-140">OUTPUTS</span></span>

### <span data-ttu-id="6caaa-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6caaa-141">System.Boolean</span></span>

## <span data-ttu-id="6caaa-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="6caaa-142">NOTES</span></span>

## <span data-ttu-id="6caaa-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6caaa-143">RELATED LINKS</span></span>
