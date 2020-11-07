---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/remove-aziotdeviceprovisioningserviceaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceAccessPolicy.md
ms.openlocfilehash: 1efd429489be41f619454fd2b772c7cbb1ebc5c7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93661123"
---
# <span data-ttu-id="d84bd-101">Remove-AzIoTDeviceProvisioningServiceAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="d84bd-101">Remove-AzIoTDeviceProvisioningServiceAccessPolicy</span></span>

## <span data-ttu-id="d84bd-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d84bd-102">SYNOPSIS</span></span>
<span data-ttu-id="d84bd-103">Löschen Sie eine freigegebene Zugriffsrichtlinie in einem Azure viel Hub-Device-Bereitstellungsdienst.</span><span class="sxs-lookup"><span data-stu-id="d84bd-103">Delete a shared access policies in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="d84bd-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d84bd-104">SYNTAX</span></span>

### <span data-ttu-id="d84bd-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="d84bd-105">ResourceSet (Default)</span></span>
```
Remove-AzIoTDeviceProvisioningServiceAccessPolicy [-ResourceGroupName] <String> [-Name] <String>
 [-KeyName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d84bd-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="d84bd-106">InputObjectSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceAccessPolicy
 [-InputObject] <PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d84bd-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="d84bd-107">ResourceIdSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceAccessPolicy [-ResourceId] <String> [-KeyName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d84bd-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d84bd-108">DESCRIPTION</span></span>
<span data-ttu-id="d84bd-109">Eine Einführung in Azure viel Hub-Device-Bereitstellungsdienst finden Sie unter https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="d84bd-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="d84bd-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d84bd-110">EXAMPLES</span></span>

### <span data-ttu-id="d84bd-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d84bd-111">Example 1</span></span>
```
PS C:\> Remove-AzIoTDeviceProvisioningServiceAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy" -PassThru

True
```

<span data-ttu-id="d84bd-112">Löschen Sie die Richtlinie für den freigegebenen Zugriff in einem azureely-Bereitstellungsdienst für Hub-Geräte.</span><span class="sxs-lookup"><span data-stu-id="d84bd-112">Delete shared access policy "mypolicy" in an Azure IoT Hub device provisioning service.</span></span>

### <span data-ttu-id="d84bd-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="d84bd-113">Example 2</span></span>
```
PS C:\> Get-AzIoTDpsAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy" | Remove-AzIoTDpsAccessPolicy
```

<span data-ttu-id="d84bd-114">Löschen Sie die Richtlinie für den freigegebenen Zugriff in einem Azure-to-Bereitstellungsdienst für Hub-Geräte mithilfe von Pipeline.</span><span class="sxs-lookup"><span data-stu-id="d84bd-114">Delete shared access policy "mypolicy" in an Azure IoT Hub device provisioning service using pipeline.</span></span>

## <span data-ttu-id="d84bd-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="d84bd-115">PARAMETERS</span></span>

### <span data-ttu-id="d84bd-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d84bd-116">-DefaultProfile</span></span>
<span data-ttu-id="d84bd-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d84bd-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d84bd-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="d84bd-118">-InputObject</span></span>
<span data-ttu-id="d84bd-119">Viel Geräte Bereitstellungsdienst Objekt</span><span class="sxs-lookup"><span data-stu-id="d84bd-119">IoT Device Provisioning Service Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d84bd-120">-KeyName</span><span class="sxs-lookup"><span data-stu-id="d84bd-120">-KeyName</span></span>
<span data-ttu-id="d84bd-121">Dienstzugriffs Richtlinien-Schlüsselname für den Geräte Bereitstellungsdienst</span><span class="sxs-lookup"><span data-stu-id="d84bd-121">IoT Device Provisioning Service access policy key name</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet, ResourceIdSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d84bd-122">-Name</span><span class="sxs-lookup"><span data-stu-id="d84bd-122">-Name</span></span>
<span data-ttu-id="d84bd-123">Name des viel Geräte Bereitstellungs Diensts</span><span class="sxs-lookup"><span data-stu-id="d84bd-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="d84bd-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d84bd-124">-PassThru</span></span>
<span data-ttu-id="d84bd-125">{{Fill passthru Description}}</span><span class="sxs-lookup"><span data-stu-id="d84bd-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="d84bd-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d84bd-126">-ResourceGroupName</span></span>
<span data-ttu-id="d84bd-127">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="d84bd-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="d84bd-128">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="d84bd-128">-ResourceId</span></span>
<span data-ttu-id="d84bd-129">Ressourcen-ID des Geräte Bereitstellungs Diensts</span><span class="sxs-lookup"><span data-stu-id="d84bd-129">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="d84bd-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d84bd-130">-Confirm</span></span>
<span data-ttu-id="d84bd-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d84bd-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d84bd-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d84bd-132">-WhatIf</span></span>
<span data-ttu-id="d84bd-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d84bd-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d84bd-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d84bd-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d84bd-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d84bd-135">CommonParameters</span></span>
<span data-ttu-id="d84bd-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d84bd-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d84bd-137">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d84bd-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d84bd-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d84bd-138">INPUTS</span></span>

### <span data-ttu-id="d84bd-139">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span><span class="sxs-lookup"><span data-stu-id="d84bd-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span></span>

### <span data-ttu-id="d84bd-140">System. String</span><span class="sxs-lookup"><span data-stu-id="d84bd-140">System.String</span></span>

## <span data-ttu-id="d84bd-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d84bd-141">OUTPUTS</span></span>

### <span data-ttu-id="d84bd-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d84bd-142">System.Boolean</span></span>

## <span data-ttu-id="d84bd-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="d84bd-143">NOTES</span></span>

## <span data-ttu-id="d84bd-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d84bd-144">RELATED LINKS</span></span>
