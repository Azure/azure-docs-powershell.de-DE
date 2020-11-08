---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/invoke-aziothubmodulemethod
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubModuleMethod.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubModuleMethod.md
ms.openlocfilehash: 818e973d4d7be9fb03e23a23d7264745920f843f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94004025"
---
# <span data-ttu-id="3fef8-101">Invoke-AzIotHubModuleMethod</span><span class="sxs-lookup"><span data-stu-id="3fef8-101">Invoke-AzIotHubModuleMethod</span></span>

## <span data-ttu-id="3fef8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3fef8-102">SYNOPSIS</span></span>
<span data-ttu-id="3fef8-103">Rufen Sie eine Edge-Modul-Methode auf.</span><span class="sxs-lookup"><span data-stu-id="3fef8-103">Invoke an Edge module method.</span></span>

## <span data-ttu-id="3fef8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3fef8-104">SYNTAX</span></span>

### <span data-ttu-id="3fef8-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="3fef8-105">ResourceSet (Default)</span></span>
```
Invoke-AzIotHubModuleMethod [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-ModuleId] <String> -Name <String> [-Payload <String>] [-ResponseTimeOut <Int32>]
 [-ConnectionTimeOut <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3fef8-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="3fef8-106">InputObjectSet</span></span>
```
Invoke-AzIotHubModuleMethod [-InputObject] <PSIotHub> [-DeviceId] <String> [-ModuleId] <String> -Name <String>
 [-Payload <String>] [-ResponseTimeOut <Int32>] [-ConnectionTimeOut <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3fef8-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="3fef8-107">ResourceIdSet</span></span>
```
Invoke-AzIotHubModuleMethod [-ResourceId] <String> [-DeviceId] <String> [-ModuleId] <String> -Name <String>
 [-Payload <String>] [-ResponseTimeOut <Int32>] [-ConnectionTimeOut <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3fef8-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3fef8-108">DESCRIPTION</span></span>
<span data-ttu-id="3fef8-109">Rufen Sie eine Edge-Modul-Methode auf.</span><span class="sxs-lookup"><span data-stu-id="3fef8-109">Invoke an Edge module method.</span></span> <span data-ttu-id="3fef8-110">Weitere Informationen finden Sie unter https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-direct-methods .</span><span class="sxs-lookup"><span data-stu-id="3fef8-110">See https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-direct-methods for more information.</span></span>

## <span data-ttu-id="3fef8-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3fef8-111">EXAMPLES</span></span>

### <span data-ttu-id="3fef8-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="3fef8-112">Example 1</span></span>
```powershell
PS C:\> Invoke-AzIotHubModuleMethod -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1" -Name "methodName" -Payload "method-input" -ResponseTimeOut 20 -ConnectionTimeOut 15
```

<span data-ttu-id="3fef8-113">Rufen Sie eine Edge-Modul-Methode auf.</span><span class="sxs-lookup"><span data-stu-id="3fef8-113">Invoke an Edge module method.</span></span>

## <span data-ttu-id="3fef8-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="3fef8-114">PARAMETERS</span></span>

### <span data-ttu-id="3fef8-115">-ConnectionTimeout</span><span class="sxs-lookup"><span data-stu-id="3fef8-115">-ConnectionTimeOut</span></span>
<span data-ttu-id="3fef8-116">Die Anzahl der Sekunden, die gewartet werden soll, bis eine Verbindung erfolgreich hergestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="3fef8-116">Number of seconds to wait until a connection is successfully made.</span></span>
<span data-ttu-id="3fef8-117">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="3fef8-117">Default is 10.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fef8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3fef8-118">-DefaultProfile</span></span>
<span data-ttu-id="3fef8-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3fef8-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fef8-120">-Geräte-Nr</span><span class="sxs-lookup"><span data-stu-id="3fef8-120">-DeviceId</span></span>
<span data-ttu-id="3fef8-121">Zielgeräte-ID.</span><span class="sxs-lookup"><span data-stu-id="3fef8-121">Target Device Id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fef8-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="3fef8-122">-InputObject</span></span>
<span data-ttu-id="3fef8-123">IotHub-Objekt</span><span class="sxs-lookup"><span data-stu-id="3fef8-123">IotHub object</span></span>

```yaml
Type: PSIotHub
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3fef8-124">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="3fef8-124">-IotHubName</span></span>
<span data-ttu-id="3fef8-125">Name des viel-Hubs</span><span class="sxs-lookup"><span data-stu-id="3fef8-125">Name of the Iot Hub</span></span>

```yaml
Type: String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fef8-126">-Modul-Nr</span><span class="sxs-lookup"><span data-stu-id="3fef8-126">-ModuleId</span></span>
<span data-ttu-id="3fef8-127">Modul-ID des Zielgeräts.</span><span class="sxs-lookup"><span data-stu-id="3fef8-127">Target device's module id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fef8-128">-Name</span><span class="sxs-lookup"><span data-stu-id="3fef8-128">-Name</span></span>
<span data-ttu-id="3fef8-129">Der Name der Methode, die für dieses Gerätemodul aufgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="3fef8-129">The name of the method to invoke on this device module.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fef8-130">-Nutzlast</span><span class="sxs-lookup"><span data-stu-id="3fef8-130">-Payload</span></span>
<span data-ttu-id="3fef8-131">Die Nutzlast für die Methode, die für dieses Gerätemodul aufgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="3fef8-131">The payload for the method to invoke on this device module.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fef8-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3fef8-132">-ResourceGroupName</span></span>
<span data-ttu-id="3fef8-133">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="3fef8-133">Name of the Resource Group</span></span>

```yaml
Type: String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fef8-134">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="3fef8-134">-ResourceId</span></span>
<span data-ttu-id="3fef8-135">IotHub-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="3fef8-135">IotHub Resource Id</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3fef8-136">-ResponseTimeOut</span><span class="sxs-lookup"><span data-stu-id="3fef8-136">-ResponseTimeOut</span></span>
<span data-ttu-id="3fef8-137">Die Anzahl der Sekunden, die gewartet werden soll, bis ein Ergebnis von der direkten Methode empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="3fef8-137">Number of seconds to wait until a result is received from the direct method.</span></span>
<span data-ttu-id="3fef8-138">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="3fef8-138">Default is 10.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fef8-139">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3fef8-139">-Confirm</span></span>
<span data-ttu-id="3fef8-140">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3fef8-140">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fef8-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3fef8-141">-WhatIf</span></span>
<span data-ttu-id="3fef8-142">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3fef8-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3fef8-143">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3fef8-143">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fef8-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3fef8-144">CommonParameters</span></span>
<span data-ttu-id="3fef8-145">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3fef8-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="3fef8-146">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3fef8-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3fef8-147">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3fef8-147">INPUTS</span></span>

### <span data-ttu-id="3fef8-148">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="3fef8-148">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="3fef8-149">System. String</span><span class="sxs-lookup"><span data-stu-id="3fef8-149">System.String</span></span>

## <span data-ttu-id="3fef8-150">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3fef8-150">OUTPUTS</span></span>

### <span data-ttu-id="3fef8-151">Microsoft. Azure. Commands. Management. IotHub. Models. PSCloudToDeviceMethodResult</span><span class="sxs-lookup"><span data-stu-id="3fef8-151">Microsoft.Azure.Commands.Management.IotHub.Models.PSCloudToDeviceMethodResult</span></span>

## <span data-ttu-id="3fef8-152">Notizen</span><span class="sxs-lookup"><span data-stu-id="3fef8-152">NOTES</span></span>

## <span data-ttu-id="3fef8-153">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3fef8-153">RELATED LINKS</span></span>
