---
external help file: Microsoft.Azure.Commands.DeviceProvisioningServices.dll-Help.xml
Module Name: AzureRM.DeviceProvisioningServices
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Remove-AzureRmIoTDeviceProvisioningServiceAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Remove-AzureRmIoTDeviceProvisioningServiceAccessPolicy.md
ms.openlocfilehash: b3a813623ed11a64a23dc35afe2f81c3f5de61da
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499530"
---
# <span data-ttu-id="9a955-101">Remove-AzureRmIoTDeviceProvisioningServiceAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="9a955-101">Remove-AzureRmIoTDeviceProvisioningServiceAccessPolicy</span></span>

## <span data-ttu-id="9a955-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9a955-102">SYNOPSIS</span></span>
<span data-ttu-id="9a955-103">Löschen Sie eine freigegebene Zugriffsrichtlinie in einem Azure viel Hub-Device-Bereitstellungsdienst.</span><span class="sxs-lookup"><span data-stu-id="9a955-103">Delete a shared access policies in an Azure IoT Hub device provisioning service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9a955-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9a955-104">SYNTAX</span></span>

### <span data-ttu-id="9a955-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="9a955-105">ResourceSet (Default)</span></span>
```
Remove-AzureRmIoTDeviceProvisioningServiceAccessPolicy [-ResourceGroupName] <String> [-Name] <String>
 [-KeyName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9a955-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="9a955-106">InputObjectSet</span></span>
```
Remove-AzureRmIoTDeviceProvisioningServiceAccessPolicy
 [-InputObject] <PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a955-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="9a955-107">ResourceIdSet</span></span>
```
Remove-AzureRmIoTDeviceProvisioningServiceAccessPolicy [-ResourceId] <String> [-KeyName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9a955-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9a955-108">DESCRIPTION</span></span>
<span data-ttu-id="9a955-109">Eine Einführung in Azure viel Hub-Device-Bereitstellungsdienst finden Sie unter https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="9a955-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="9a955-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9a955-110">EXAMPLES</span></span>

### <span data-ttu-id="9a955-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="9a955-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmIoTDeviceProvisioningServiceAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy" -PassThru

True
```

<span data-ttu-id="9a955-112">Löschen Sie die Richtlinie für den freigegebenen Zugriff in einem azureely-Bereitstellungsdienst für Hub-Geräte.</span><span class="sxs-lookup"><span data-stu-id="9a955-112">Delete shared access policy "mypolicy" in an Azure IoT Hub device provisioning service.</span></span>

### <span data-ttu-id="9a955-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="9a955-113">Example 2</span></span>
```
PS C:\> Get-AzureRmIoTDpsAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy" | Remove-AzureRmIoTDpsAccessPolicy
```

<span data-ttu-id="9a955-114">Löschen Sie die Richtlinie für den freigegebenen Zugriff in einem Azure-to-Bereitstellungsdienst für Hub-Geräte mithilfe von Pipeline.</span><span class="sxs-lookup"><span data-stu-id="9a955-114">Delete shared access policy "mypolicy" in an Azure IoT Hub device provisioning service using pipeline.</span></span>

## <span data-ttu-id="9a955-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="9a955-115">PARAMETERS</span></span>

### <span data-ttu-id="9a955-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a955-116">-DefaultProfile</span></span>
<span data-ttu-id="9a955-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9a955-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a955-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="9a955-118">-InputObject</span></span>
<span data-ttu-id="9a955-119">Viel Geräte Bereitstellungsdienst Objekt</span><span class="sxs-lookup"><span data-stu-id="9a955-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="9a955-120">-KeyName</span><span class="sxs-lookup"><span data-stu-id="9a955-120">-KeyName</span></span>
<span data-ttu-id="9a955-121">Dienstzugriffs Richtlinien-Schlüsselname für den Geräte Bereitstellungsdienst</span><span class="sxs-lookup"><span data-stu-id="9a955-121">IoT Device Provisioning Service access policy key name</span></span>

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

### <span data-ttu-id="9a955-122">-Name</span><span class="sxs-lookup"><span data-stu-id="9a955-122">-Name</span></span>
<span data-ttu-id="9a955-123">Name des viel Geräte Bereitstellungs Diensts</span><span class="sxs-lookup"><span data-stu-id="9a955-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="9a955-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9a955-124">-PassThru</span></span>
<span data-ttu-id="9a955-125">{{Fill passthru Description}}</span><span class="sxs-lookup"><span data-stu-id="9a955-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="9a955-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9a955-126">-ResourceGroupName</span></span>
<span data-ttu-id="9a955-127">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="9a955-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="9a955-128">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="9a955-128">-ResourceId</span></span>
<span data-ttu-id="9a955-129">Ressourcen-ID des Geräte Bereitstellungs Diensts</span><span class="sxs-lookup"><span data-stu-id="9a955-129">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="9a955-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9a955-130">-Confirm</span></span>
<span data-ttu-id="9a955-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9a955-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9a955-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9a955-132">-WhatIf</span></span>
<span data-ttu-id="9a955-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9a955-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9a955-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9a955-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9a955-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a955-135">CommonParameters</span></span>
<span data-ttu-id="9a955-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a955-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a955-137">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9a955-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a955-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9a955-138">INPUTS</span></span>

### <span data-ttu-id="9a955-139">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span><span class="sxs-lookup"><span data-stu-id="9a955-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span></span>
<span data-ttu-id="9a955-140">Parameter: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="9a955-140">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="9a955-141">System. String</span><span class="sxs-lookup"><span data-stu-id="9a955-141">System.String</span></span>

## <span data-ttu-id="9a955-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9a955-142">OUTPUTS</span></span>

### <span data-ttu-id="9a955-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9a955-143">System.Boolean</span></span>

## <span data-ttu-id="9a955-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="9a955-144">NOTES</span></span>

## <span data-ttu-id="9a955-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9a955-145">RELATED LINKS</span></span>
