---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/add-azurermiothubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Add-AzureRmIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Add-AzureRmIotHubKey.md
ms.openlocfilehash: 379aaa360776291515f1848cd48b24e88be23ef6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496086"
---
# <span data-ttu-id="e499d-101">Add-AzureRmIotHubKey</span><span class="sxs-lookup"><span data-stu-id="e499d-101">Add-AzureRmIotHubKey</span></span>

## <span data-ttu-id="e499d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e499d-102">SYNOPSIS</span></span>
<span data-ttu-id="e499d-103">Erstellt einen IotHub-Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="e499d-103">Creates an IotHub Key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e499d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e499d-104">SYNTAX</span></span>

```
Add-AzureRmIotHubKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String> [-PrimaryKey <String>]
 [-SecondaryKey <String>] -Rights <PSAccessRights> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e499d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e499d-105">DESCRIPTION</span></span>
<span data-ttu-id="e499d-106">Erstellt einen Schlüssel für den bereitgestellten IotHub.</span><span class="sxs-lookup"><span data-stu-id="e499d-106">Creates a Key for the provided IotHub.</span></span>
<span data-ttu-id="e499d-107">Keynames sind nicht eindeutig und müssen sorgfältig verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="e499d-107">KeyNames are not unique and need to be managed carefully.</span></span>

## <span data-ttu-id="e499d-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e499d-108">EXAMPLES</span></span>

### <span data-ttu-id="e499d-109">Beispiel 1 Hinzufügen eines Schlüssels zu einem IotHub</span><span class="sxs-lookup"><span data-stu-id="e499d-109">Example 1 Add a Key to an IotHub</span></span>
```
PS C:\> Add-AzureRmIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "newkey" -PrimaryKey "primarykey" -SecondaryKey "secondarykey" -Rights RegistryRead
```

<span data-ttu-id="e499d-110">Erstellt einen Schlüssel mit dem Namen "MyKey" für die iothub "myiothub" mit RegistryRead-Berechtigungen.</span><span class="sxs-lookup"><span data-stu-id="e499d-110">Creates a key named "mykey" for the iothub "myiothub" with RegistryRead permissions.</span></span>

## <span data-ttu-id="e499d-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="e499d-111">PARAMETERS</span></span>

### <span data-ttu-id="e499d-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e499d-112">-DefaultProfile</span></span>
<span data-ttu-id="e499d-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="e499d-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e499d-114">-KeyName</span><span class="sxs-lookup"><span data-stu-id="e499d-114">-KeyName</span></span>
<span data-ttu-id="e499d-115">Name des Schlüssels</span><span class="sxs-lookup"><span data-stu-id="e499d-115">Name of the Key</span></span>

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

### <span data-ttu-id="e499d-116">-Name</span><span class="sxs-lookup"><span data-stu-id="e499d-116">-Name</span></span>
<span data-ttu-id="e499d-117">Name des IotHub</span><span class="sxs-lookup"><span data-stu-id="e499d-117">Name of the IotHub</span></span>

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

### <span data-ttu-id="e499d-118">-Primär Primär</span><span class="sxs-lookup"><span data-stu-id="e499d-118">-PrimaryKey</span></span>
<span data-ttu-id="e499d-119">Der Primärschlüssel</span><span class="sxs-lookup"><span data-stu-id="e499d-119">The primary key</span></span>

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

### <span data-ttu-id="e499d-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e499d-120">-ResourceGroupName</span></span>
<span data-ttu-id="e499d-121">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="e499d-121">Resource Group Name</span></span>

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

### <span data-ttu-id="e499d-122">-Rechte</span><span class="sxs-lookup"><span data-stu-id="e499d-122">-Rights</span></span>
<span data-ttu-id="e499d-123">Die Berechtigungen für diesen IOTHub</span><span class="sxs-lookup"><span data-stu-id="e499d-123">The permissions for this IOTHub</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSAccessRights
Parameter Sets: (All)
Aliases:
Accepted values: RegistryRead, RegistryWrite, ServiceConnect, DeviceConnect

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e499d-124">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="e499d-124">-SecondaryKey</span></span>
<span data-ttu-id="e499d-125">Der sekundäre Schlüssel</span><span class="sxs-lookup"><span data-stu-id="e499d-125">The Secondary Key</span></span>

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

### <span data-ttu-id="e499d-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e499d-126">-Confirm</span></span>
<span data-ttu-id="e499d-127">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e499d-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e499d-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e499d-128">-WhatIf</span></span>
<span data-ttu-id="e499d-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e499d-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e499d-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e499d-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e499d-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e499d-131">CommonParameters</span></span>
<span data-ttu-id="e499d-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e499d-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e499d-133">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e499d-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e499d-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e499d-134">INPUTS</span></span>

### <span data-ttu-id="e499d-135">System. String</span><span class="sxs-lookup"><span data-stu-id="e499d-135">System.String</span></span>

## <span data-ttu-id="e499d-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e499d-136">OUTPUTS</span></span>

### <span data-ttu-id="e499d-137">Microsoft. Azure. Commands. Management. IotHub. Models. PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="e499d-137">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="e499d-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="e499d-138">NOTES</span></span>

## <span data-ttu-id="e499d-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e499d-139">RELATED LINKS</span></span>
