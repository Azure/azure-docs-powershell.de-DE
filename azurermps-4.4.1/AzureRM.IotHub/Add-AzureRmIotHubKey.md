---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Add-AzureRmIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Add-AzureRmIotHubKey.md
ms.openlocfilehash: f7bbe0c37d03a6db372c6c70da021160060a542a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501834"
---
# <span data-ttu-id="1336b-101">Add-AzureRmIotHubKey</span><span class="sxs-lookup"><span data-stu-id="1336b-101">Add-AzureRmIotHubKey</span></span>

## <span data-ttu-id="1336b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1336b-102">SYNOPSIS</span></span>
<span data-ttu-id="1336b-103">Erstellt einen IotHub-Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="1336b-103">Creates an IotHub Key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1336b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1336b-104">SYNTAX</span></span>

```
Add-AzureRmIotHubKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String>
 [[-PrimaryKey] <String>] [[-SecondaryKey] <String>] [-Rights] <PSAccessRights>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1336b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1336b-105">DESCRIPTION</span></span>
<span data-ttu-id="1336b-106">Erstellt einen Schlüssel für den bereitgestellten IotHub.</span><span class="sxs-lookup"><span data-stu-id="1336b-106">Creates a Key for the provided IotHub.</span></span>
<span data-ttu-id="1336b-107">Keynames sind nicht eindeutig und müssen sorgfältig verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="1336b-107">KeyNames are not unique and need to be managed carefully.</span></span>

## <span data-ttu-id="1336b-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1336b-108">EXAMPLES</span></span>

### <span data-ttu-id="1336b-109">Beispiel 1 Hinzufügen eines Schlüssels zu einem IotHub</span><span class="sxs-lookup"><span data-stu-id="1336b-109">Example 1 Add a Key to an IotHub</span></span>
```
PS C:\> Add-AzureRmIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "newkey" -PrimaryKey "primarykey" -SecondaryKey "secondarykey" -Rights RegistryRead
```

<span data-ttu-id="1336b-110">Erstellt einen Schlüssel mit dem Namen "MyKey" für die iothub "myiothub" mit RegistryRead-Berechtigungen.</span><span class="sxs-lookup"><span data-stu-id="1336b-110">Creates a key named "mykey" for the iothub "myiothub" with RegistryRead permissions.</span></span>

## <span data-ttu-id="1336b-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="1336b-111">PARAMETERS</span></span>

### <span data-ttu-id="1336b-112">-KeyName</span><span class="sxs-lookup"><span data-stu-id="1336b-112">-KeyName</span></span>
<span data-ttu-id="1336b-113">Name des Schlüssels</span><span class="sxs-lookup"><span data-stu-id="1336b-113">Name of the Key</span></span>

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

### <span data-ttu-id="1336b-114">-Name</span><span class="sxs-lookup"><span data-stu-id="1336b-114">-Name</span></span>
<span data-ttu-id="1336b-115">Name des IotHub</span><span class="sxs-lookup"><span data-stu-id="1336b-115">Name of the IotHub</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1336b-116">-Primär Primär</span><span class="sxs-lookup"><span data-stu-id="1336b-116">-PrimaryKey</span></span>
<span data-ttu-id="1336b-117">Der Primärschlüssel</span><span class="sxs-lookup"><span data-stu-id="1336b-117">The primary key</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1336b-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1336b-118">-ResourceGroupName</span></span>
<span data-ttu-id="1336b-119">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="1336b-119">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1336b-120">-Rechte</span><span class="sxs-lookup"><span data-stu-id="1336b-120">-Rights</span></span>
<span data-ttu-id="1336b-121">Die Berechtigungen für diesen IOTHub</span><span class="sxs-lookup"><span data-stu-id="1336b-121">The permissions for this IOTHub</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSAccessRights
Parameter Sets: (All)
Aliases: 
Accepted values: RegistryRead, RegistryWrite, ServiceConnect, DeviceConnect

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1336b-122">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="1336b-122">-SecondaryKey</span></span>
<span data-ttu-id="1336b-123">Der sekundäre Schlüssel</span><span class="sxs-lookup"><span data-stu-id="1336b-123">The Secondary Key</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1336b-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1336b-124">-Confirm</span></span>
<span data-ttu-id="1336b-125">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1336b-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1336b-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1336b-126">-WhatIf</span></span>
<span data-ttu-id="1336b-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1336b-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1336b-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1336b-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1336b-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1336b-129">-DefaultProfile</span></span>
<span data-ttu-id="1336b-130">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1336b-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1336b-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1336b-131">CommonParameters</span></span>
<span data-ttu-id="1336b-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1336b-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1336b-133">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1336b-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1336b-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1336b-134">INPUTS</span></span>

### <span data-ttu-id="1336b-135">System. String</span><span class="sxs-lookup"><span data-stu-id="1336b-135">System.String</span></span>
<span data-ttu-id="1336b-136">Microsoft. Azure. Commands. Management. IotHub. Models. PSAccessRights</span><span class="sxs-lookup"><span data-stu-id="1336b-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSAccessRights</span></span>

## <span data-ttu-id="1336b-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1336b-137">OUTPUTS</span></span>

### <span data-ttu-id="1336b-138">Microsoft. Azure. Commands. Management. IotHub. Models. PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="1336b-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>
<span data-ttu-id="1336b-139">System. Collections. Generic. List \` 1 \[ \[ Microsoft. Azure. Commands. Management. IotHub. Models. PSSharedAccessSignatureAuthorizationRule, Microsoft. Azure. Commands. IotHub, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null\]\]</span><span class="sxs-lookup"><span data-stu-id="1336b-139">System.Collections.Generic.List\`1\[\[Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule, Microsoft.Azure.Commands.IotHub, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null\]\]</span></span>

## <span data-ttu-id="1336b-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="1336b-140">NOTES</span></span>

## <span data-ttu-id="1336b-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1336b-141">RELATED LINKS</span></span>

