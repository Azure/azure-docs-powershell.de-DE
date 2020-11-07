---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubKey.md
ms.openlocfilehash: f73cfd1cadff449289bfa82ab1de04d110fb0f1a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93819811"
---
# <span data-ttu-id="a1afd-101">Add-AzIotHubKey</span><span class="sxs-lookup"><span data-stu-id="a1afd-101">Add-AzIotHubKey</span></span>

## <span data-ttu-id="a1afd-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a1afd-102">SYNOPSIS</span></span>
<span data-ttu-id="a1afd-103">Erstellt einen IotHub-Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="a1afd-103">Creates an IotHub Key.</span></span>

## <span data-ttu-id="a1afd-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a1afd-104">SYNTAX</span></span>

```
Add-AzIotHubKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String> [-PrimaryKey <String>]
 [-SecondaryKey <String>] -Rights <PSAccessRights> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a1afd-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a1afd-105">DESCRIPTION</span></span>
<span data-ttu-id="a1afd-106">Erstellt einen Schlüssel für den bereitgestellten IotHub.</span><span class="sxs-lookup"><span data-stu-id="a1afd-106">Creates a Key for the provided IotHub.</span></span>
<span data-ttu-id="a1afd-107">Keynames sind nicht eindeutig und müssen sorgfältig verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="a1afd-107">KeyNames are not unique and need to be managed carefully.</span></span>

## <span data-ttu-id="a1afd-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a1afd-108">EXAMPLES</span></span>

### <span data-ttu-id="a1afd-109">Beispiel 1 Hinzufügen eines Schlüssels zu einem IotHub</span><span class="sxs-lookup"><span data-stu-id="a1afd-109">Example 1 Add a Key to an IotHub</span></span>
```
PS C:\> Add-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "newkey" -PrimaryKey "primarykey" -SecondaryKey "secondarykey" -Rights RegistryRead
```

<span data-ttu-id="a1afd-110">Erstellt einen Schlüssel mit dem Namen "MyKey" für die iothub "myiothub" mit RegistryRead-Berechtigungen.</span><span class="sxs-lookup"><span data-stu-id="a1afd-110">Creates a key named "mykey" for the iothub "myiothub" with RegistryRead permissions.</span></span>

## <span data-ttu-id="a1afd-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="a1afd-111">PARAMETERS</span></span>

### <span data-ttu-id="a1afd-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1afd-112">-DefaultProfile</span></span>
<span data-ttu-id="a1afd-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="a1afd-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a1afd-114">-KeyName</span><span class="sxs-lookup"><span data-stu-id="a1afd-114">-KeyName</span></span>
<span data-ttu-id="a1afd-115">Name des Schlüssels</span><span class="sxs-lookup"><span data-stu-id="a1afd-115">Name of the Key</span></span>

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

### <span data-ttu-id="a1afd-116">-Name</span><span class="sxs-lookup"><span data-stu-id="a1afd-116">-Name</span></span>
<span data-ttu-id="a1afd-117">Name des IotHub</span><span class="sxs-lookup"><span data-stu-id="a1afd-117">Name of the IotHub</span></span>

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

### <span data-ttu-id="a1afd-118">-Primär Primär</span><span class="sxs-lookup"><span data-stu-id="a1afd-118">-PrimaryKey</span></span>
<span data-ttu-id="a1afd-119">Der Primärschlüssel</span><span class="sxs-lookup"><span data-stu-id="a1afd-119">The primary key</span></span>

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

### <span data-ttu-id="a1afd-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1afd-120">-ResourceGroupName</span></span>
<span data-ttu-id="a1afd-121">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="a1afd-121">Resource Group Name</span></span>

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

### <span data-ttu-id="a1afd-122">-Rechte</span><span class="sxs-lookup"><span data-stu-id="a1afd-122">-Rights</span></span>
<span data-ttu-id="a1afd-123">Die Berechtigungen für diesen IOTHub</span><span class="sxs-lookup"><span data-stu-id="a1afd-123">The permissions for this IOTHub</span></span>

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

### <span data-ttu-id="a1afd-124">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="a1afd-124">-SecondaryKey</span></span>
<span data-ttu-id="a1afd-125">Der sekundäre Schlüssel</span><span class="sxs-lookup"><span data-stu-id="a1afd-125">The Secondary Key</span></span>

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

### <span data-ttu-id="a1afd-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a1afd-126">-Confirm</span></span>
<span data-ttu-id="a1afd-127">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a1afd-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a1afd-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a1afd-128">-WhatIf</span></span>
<span data-ttu-id="a1afd-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a1afd-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a1afd-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a1afd-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a1afd-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1afd-131">CommonParameters</span></span>
<span data-ttu-id="a1afd-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1afd-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1afd-133">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1afd-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1afd-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a1afd-134">INPUTS</span></span>

### <span data-ttu-id="a1afd-135">System. String</span><span class="sxs-lookup"><span data-stu-id="a1afd-135">System.String</span></span>

## <span data-ttu-id="a1afd-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a1afd-136">OUTPUTS</span></span>

### <span data-ttu-id="a1afd-137">Microsoft. Azure. Commands. Management. IotHub. Models. PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="a1afd-137">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="a1afd-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="a1afd-138">NOTES</span></span>

## <span data-ttu-id="a1afd-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a1afd-139">RELATED LINKS</span></span>
