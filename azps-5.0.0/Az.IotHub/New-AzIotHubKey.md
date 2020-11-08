---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/new-aziothubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHubKey.md
ms.openlocfilehash: cc843ca942ae79fe76e1dd50e76c876e4d05b5ac
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94177944"
---
# <span data-ttu-id="8fcf5-101">New-AzIotHubKey</span><span class="sxs-lookup"><span data-stu-id="8fcf5-101">New-AzIotHubKey</span></span>

## <span data-ttu-id="8fcf5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8fcf5-102">SYNOPSIS</span></span>
<span data-ttu-id="8fcf5-103">Generieren Sie einen Azure-viel-Hub-Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="8fcf5-103">Generate an Azure IoT Hub key.</span></span>

## <span data-ttu-id="8fcf5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8fcf5-104">SYNTAX</span></span>

### <span data-ttu-id="8fcf5-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="8fcf5-105">ResourceSet (Default)</span></span>
```
New-AzIotHubKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String> [-RenewKey] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8fcf5-106">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="8fcf5-106">ResourceIdSet</span></span>
```
New-AzIotHubKey [-HubId] <String> [-KeyName] <String> [-RenewKey] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8fcf5-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8fcf5-107">DESCRIPTION</span></span>
<span data-ttu-id="8fcf5-108">Generieren Sie einen Azure-viel-Hub-Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="8fcf5-108">Generate an Azure IoT Hub key.</span></span>

## <span data-ttu-id="8fcf5-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8fcf5-109">EXAMPLES</span></span>

### <span data-ttu-id="8fcf5-110">Beispiel 1 regenerieren des Primärschlüssels</span><span class="sxs-lookup"><span data-stu-id="8fcf5-110">Example 1 Regenerate primary key</span></span>
```
PS C:\> New-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "testKey" -RenewKey "primary"

KeyName     PrimaryKey                                      SecondaryKey                                        Rights
-------     ----------                                      ------------                                        ------
test        SXSdm31aT+i3939xSnA191f8g3uRhIUCTsO26b9s/nE=    6JqGKGUTL0mhQwvcOeIRT7OnT6noK/tie6jBY77sJTE=        ServiceConnect
```

<span data-ttu-id="8fcf5-111">Neu generierter Primärschlüssel für die Autorisierungsrichtlinie "testKey" eines Azure viel-Hubs.</span><span class="sxs-lookup"><span data-stu-id="8fcf5-111">Regenerated primary key for the authorization policy "testKey" of an azure iot hub.</span></span>

### <span data-ttu-id="8fcf5-112">Beispiel 2 tauschen von Schlüsseln</span><span class="sxs-lookup"><span data-stu-id="8fcf5-112">Example 2 Swapping keys</span></span>
```
PS C:\> New-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "testKey" -RenewKey "swap"

KeyName     PrimaryKey                                      SecondaryKey                                        Rights
-------     ----------                                      ------------                                        ------
test        6JqGKGUTL0mhQwvcOeIRT7OnT6noK/tie6jBY77sJTE=    SXSdm31aT+i3939xSnA191f8g3uRhIUCTsO26b9s/nE=        ServiceConnect
```

<span data-ttu-id="8fcf5-113">Tauschen Sie die Schlüssel für die Autorisierungsrichtlinie "testKey" eines Azure-viel-Hubs aus.</span><span class="sxs-lookup"><span data-stu-id="8fcf5-113">Swapping keys for the authorization policy "testKey" of an azure iot hub.</span></span>

## <span data-ttu-id="8fcf5-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="8fcf5-114">PARAMETERS</span></span>

### <span data-ttu-id="8fcf5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8fcf5-115">-DefaultProfile</span></span>
<span data-ttu-id="8fcf5-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="8fcf5-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8fcf5-117">-HubId</span><span class="sxs-lookup"><span data-stu-id="8fcf5-117">-HubId</span></span>
<span data-ttu-id="8fcf5-118">IotHub-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="8fcf5-118">IotHub Resource Id</span></span>

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

### <span data-ttu-id="8fcf5-119">-KeyName</span><span class="sxs-lookup"><span data-stu-id="8fcf5-119">-KeyName</span></span>
<span data-ttu-id="8fcf5-120">Name des Schlüssels</span><span class="sxs-lookup"><span data-stu-id="8fcf5-120">Name of the Key</span></span>

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

### <span data-ttu-id="8fcf5-121">-Name</span><span class="sxs-lookup"><span data-stu-id="8fcf5-121">-Name</span></span>
<span data-ttu-id="8fcf5-122">Name des IotHub</span><span class="sxs-lookup"><span data-stu-id="8fcf5-122">Name of the IotHub</span></span>

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

### <span data-ttu-id="8fcf5-123">-RenewKey</span><span class="sxs-lookup"><span data-stu-id="8fcf5-123">-RenewKey</span></span>
<span data-ttu-id="8fcf5-124">Schlüssel neu generieren</span><span class="sxs-lookup"><span data-stu-id="8fcf5-124">Regenerate Key.</span></span>

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

### <span data-ttu-id="8fcf5-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8fcf5-125">-ResourceGroupName</span></span>
<span data-ttu-id="8fcf5-126">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="8fcf5-126">Resource Group Name</span></span>

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

### <span data-ttu-id="8fcf5-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8fcf5-127">-Confirm</span></span>
<span data-ttu-id="8fcf5-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8fcf5-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8fcf5-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8fcf5-129">-WhatIf</span></span>
<span data-ttu-id="8fcf5-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8fcf5-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8fcf5-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8fcf5-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8fcf5-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8fcf5-132">CommonParameters</span></span>
<span data-ttu-id="8fcf5-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8fcf5-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8fcf5-134">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8fcf5-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8fcf5-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8fcf5-135">INPUTS</span></span>

### <span data-ttu-id="8fcf5-136">System. String</span><span class="sxs-lookup"><span data-stu-id="8fcf5-136">System.String</span></span>

## <span data-ttu-id="8fcf5-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8fcf5-137">OUTPUTS</span></span>

### <span data-ttu-id="8fcf5-138">Microsoft. Azure. Commands. Management. IotHub. Models. PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="8fcf5-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="8fcf5-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="8fcf5-139">NOTES</span></span>

## <span data-ttu-id="8fcf5-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8fcf5-140">RELATED LINKS</span></span>
