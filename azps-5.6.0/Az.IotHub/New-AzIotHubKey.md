---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/new-aziothubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHubKey.md
ms.openlocfilehash: 7dd27544e3304570cf3fbdae861b21eabd300c35
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101927104"
---
# <span data-ttu-id="fe78c-101">New-AzIotHubKey</span><span class="sxs-lookup"><span data-stu-id="fe78c-101">New-AzIotHubKey</span></span>

## <span data-ttu-id="fe78c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fe78c-102">SYNOPSIS</span></span>
<span data-ttu-id="fe78c-103">Generieren Sie einen Azure IoT Hub-Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="fe78c-103">Generate an Azure IoT Hub key.</span></span>

## <span data-ttu-id="fe78c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fe78c-104">SYNTAX</span></span>

### <span data-ttu-id="fe78c-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="fe78c-105">ResourceSet (Default)</span></span>
```
New-AzIotHubKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String> [-RenewKey] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe78c-106">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="fe78c-106">ResourceIdSet</span></span>
```
New-AzIotHubKey [-HubId] <String> [-KeyName] <String> [-RenewKey] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fe78c-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fe78c-107">DESCRIPTION</span></span>
<span data-ttu-id="fe78c-108">Generieren Sie einen Azure IoT Hub-Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="fe78c-108">Generate an Azure IoT Hub key.</span></span>

## <span data-ttu-id="fe78c-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="fe78c-109">EXAMPLES</span></span>

### <span data-ttu-id="fe78c-110">Beispiel 1 Neuerieren des Primärschlüssels</span><span class="sxs-lookup"><span data-stu-id="fe78c-110">Example 1 Regenerate primary key</span></span>
```
PS C:\> New-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "testKey" -RenewKey "primary"

KeyName     PrimaryKey                                      SecondaryKey                                        Rights
-------     ----------                                      ------------                                        ------
test        SXSdm31aT+i3939xSnA191f8g3uRhIUCTsO26b9s/nE=    6JqGKGUTL0mhQwvcOeIRT7OnT6noK/tie6jBY77sJTE=        ServiceConnect
```

<span data-ttu-id="fe78c-111">Neu generierter Primärschlüssel für die Autorisierungsrichtlinie "testKey" eines azure iot-Hubs.</span><span class="sxs-lookup"><span data-stu-id="fe78c-111">Regenerated primary key for the authorization policy "testKey" of an azure iot hub.</span></span>

### <span data-ttu-id="fe78c-112">Beispiel 2 Tauschtasten</span><span class="sxs-lookup"><span data-stu-id="fe78c-112">Example 2 Swapping keys</span></span>
```
PS C:\> New-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "testKey" -RenewKey "swap"

KeyName     PrimaryKey                                      SecondaryKey                                        Rights
-------     ----------                                      ------------                                        ------
test        6JqGKGUTL0mhQwvcOeIRT7OnT6noK/tie6jBY77sJTE=    SXSdm31aT+i3939xSnA191f8g3uRhIUCTsO26b9s/nE=        ServiceConnect
```

<span data-ttu-id="fe78c-113">Austauschen von Schlüsseln für die Autorisierungsrichtlinie "testKey" eines azure iot-Hubs.</span><span class="sxs-lookup"><span data-stu-id="fe78c-113">Swapping keys for the authorization policy "testKey" of an azure iot hub.</span></span>

## <span data-ttu-id="fe78c-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="fe78c-114">PARAMETERS</span></span>

### <span data-ttu-id="fe78c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe78c-115">-DefaultProfile</span></span>
<span data-ttu-id="fe78c-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="fe78c-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fe78c-117">-HubId</span><span class="sxs-lookup"><span data-stu-id="fe78c-117">-HubId</span></span>
<span data-ttu-id="fe78c-118">IotHub-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="fe78c-118">IotHub Resource Id</span></span>

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

### <span data-ttu-id="fe78c-119">-KeyName</span><span class="sxs-lookup"><span data-stu-id="fe78c-119">-KeyName</span></span>
<span data-ttu-id="fe78c-120">Name des Schlüssels</span><span class="sxs-lookup"><span data-stu-id="fe78c-120">Name of the Key</span></span>

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

### <span data-ttu-id="fe78c-121">-Name</span><span class="sxs-lookup"><span data-stu-id="fe78c-121">-Name</span></span>
<span data-ttu-id="fe78c-122">Name des IotHub</span><span class="sxs-lookup"><span data-stu-id="fe78c-122">Name of the IotHub</span></span>

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

### <span data-ttu-id="fe78c-123">-RenewKey</span><span class="sxs-lookup"><span data-stu-id="fe78c-123">-RenewKey</span></span>
<span data-ttu-id="fe78c-124">Schlüssel regenerieren.</span><span class="sxs-lookup"><span data-stu-id="fe78c-124">Regenerate Key.</span></span>

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

### <span data-ttu-id="fe78c-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe78c-125">-ResourceGroupName</span></span>
<span data-ttu-id="fe78c-126">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="fe78c-126">Resource Group Name</span></span>

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

### <span data-ttu-id="fe78c-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="fe78c-127">-Confirm</span></span>
<span data-ttu-id="fe78c-128">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="fe78c-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fe78c-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe78c-129">-WhatIf</span></span>
<span data-ttu-id="fe78c-130">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fe78c-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fe78c-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fe78c-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fe78c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe78c-132">CommonParameters</span></span>
<span data-ttu-id="fe78c-133">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe78c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe78c-134">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe78c-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe78c-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="fe78c-135">INPUTS</span></span>

### <span data-ttu-id="fe78c-136">System.String</span><span class="sxs-lookup"><span data-stu-id="fe78c-136">System.String</span></span>

## <span data-ttu-id="fe78c-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="fe78c-137">OUTPUTS</span></span>

### <span data-ttu-id="fe78c-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="fe78c-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="fe78c-139">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="fe78c-139">NOTES</span></span>

## <span data-ttu-id="fe78c-140">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="fe78c-140">RELATED LINKS</span></span>
