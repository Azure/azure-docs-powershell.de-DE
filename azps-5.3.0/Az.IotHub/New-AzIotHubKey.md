---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/new-aziothubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHubKey.md
ms.openlocfilehash: cc843ca942ae79fe76e1dd50e76c876e4d05b5ac
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98472470"
---
# <span data-ttu-id="36846-101">New-AzIotHubKey</span><span class="sxs-lookup"><span data-stu-id="36846-101">New-AzIotHubKey</span></span>

## <span data-ttu-id="36846-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="36846-102">SYNOPSIS</span></span>
<span data-ttu-id="36846-103">Generieren Sie einen Azure IoT Hub-Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="36846-103">Generate an Azure IoT Hub key.</span></span>

## <span data-ttu-id="36846-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="36846-104">SYNTAX</span></span>

### <span data-ttu-id="36846-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="36846-105">ResourceSet (Default)</span></span>
```
New-AzIotHubKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String> [-RenewKey] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36846-106">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="36846-106">ResourceIdSet</span></span>
```
New-AzIotHubKey [-HubId] <String> [-KeyName] <String> [-RenewKey] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="36846-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="36846-107">DESCRIPTION</span></span>
<span data-ttu-id="36846-108">Generieren Sie einen Azure IoT Hub-Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="36846-108">Generate an Azure IoT Hub key.</span></span>

## <span data-ttu-id="36846-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="36846-109">EXAMPLES</span></span>

### <span data-ttu-id="36846-110">Beispiel 1: Erneut generierter Primärschlüssel</span><span class="sxs-lookup"><span data-stu-id="36846-110">Example 1 Regenerate primary key</span></span>
```
PS C:\> New-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "testKey" -RenewKey "primary"

KeyName     PrimaryKey                                      SecondaryKey                                        Rights
-------     ----------                                      ------------                                        ------
test        SXSdm31aT+i3939xSnA191f8g3uRhIUCTsO26b9s/nE=    6JqGKGUTL0mhQwvcOeIRT7OnT6noK/tie6jBY77sJTE=        ServiceConnect
```

<span data-ttu-id="36846-111">Generierter Primärschlüssel für die Autorisierungsrichtlinie "testKey" eines Azure iot-Hubs.</span><span class="sxs-lookup"><span data-stu-id="36846-111">Regenerated primary key for the authorization policy "testKey" of an azure iot hub.</span></span>

### <span data-ttu-id="36846-112">Beispiel 2 Austauschen von Schlüsseln</span><span class="sxs-lookup"><span data-stu-id="36846-112">Example 2 Swapping keys</span></span>
```
PS C:\> New-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "testKey" -RenewKey "swap"

KeyName     PrimaryKey                                      SecondaryKey                                        Rights
-------     ----------                                      ------------                                        ------
test        6JqGKGUTL0mhQwvcOeIRT7OnT6noK/tie6jBY77sJTE=    SXSdm31aT+i3939xSnA191f8g3uRhIUCTsO26b9s/nE=        ServiceConnect
```

<span data-ttu-id="36846-113">Austauschen von Schlüsseln für die Autorisierungsrichtlinie "testKey" eines Azure iot-Hubs.</span><span class="sxs-lookup"><span data-stu-id="36846-113">Swapping keys for the authorization policy "testKey" of an azure iot hub.</span></span>

## <span data-ttu-id="36846-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="36846-114">PARAMETERS</span></span>

### <span data-ttu-id="36846-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36846-115">-DefaultProfile</span></span>
<span data-ttu-id="36846-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="36846-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="36846-117">-HubId</span><span class="sxs-lookup"><span data-stu-id="36846-117">-HubId</span></span>
<span data-ttu-id="36846-118">IotHub-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="36846-118">IotHub Resource Id</span></span>

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

### <span data-ttu-id="36846-119">-KeyName</span><span class="sxs-lookup"><span data-stu-id="36846-119">-KeyName</span></span>
<span data-ttu-id="36846-120">Name des Schlüssels</span><span class="sxs-lookup"><span data-stu-id="36846-120">Name of the Key</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36846-121">-Name</span><span class="sxs-lookup"><span data-stu-id="36846-121">-Name</span></span>
<span data-ttu-id="36846-122">Name des IotHub</span><span class="sxs-lookup"><span data-stu-id="36846-122">Name of the IotHub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36846-123">-RenewKey</span><span class="sxs-lookup"><span data-stu-id="36846-123">-RenewKey</span></span>
<span data-ttu-id="36846-124">Schlüssel erneut generiert.</span><span class="sxs-lookup"><span data-stu-id="36846-124">Regenerate Key.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36846-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36846-125">-ResourceGroupName</span></span>
<span data-ttu-id="36846-126">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="36846-126">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36846-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="36846-127">-Confirm</span></span>
<span data-ttu-id="36846-128">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="36846-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36846-129">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="36846-129">-WhatIf</span></span>
<span data-ttu-id="36846-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="36846-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="36846-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="36846-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36846-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36846-132">CommonParameters</span></span>
<span data-ttu-id="36846-133">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36846-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36846-134">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36846-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36846-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="36846-135">INPUTS</span></span>

### <span data-ttu-id="36846-136">System.String</span><span class="sxs-lookup"><span data-stu-id="36846-136">System.String</span></span>

## <span data-ttu-id="36846-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="36846-137">OUTPUTS</span></span>

### <span data-ttu-id="36846-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="36846-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="36846-139">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="36846-139">NOTES</span></span>

## <span data-ttu-id="36846-140">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="36846-140">RELATED LINKS</span></span>
