---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Add-AzIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Add-AzIotHubKey.md
ms.openlocfilehash: 75f623890963095efbf37a631bf4c0736245fe28
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843976"
---
# <span data-ttu-id="eeb03-101">Add-AzIotHubKey</span><span class="sxs-lookup"><span data-stu-id="eeb03-101">Add-AzIotHubKey</span></span>

## <span data-ttu-id="eeb03-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="eeb03-102">SYNOPSIS</span></span>
<span data-ttu-id="eeb03-103">Erstellt einen IotHub-Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="eeb03-103">Creates an IotHub Key.</span></span>

## <span data-ttu-id="eeb03-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="eeb03-104">SYNTAX</span></span>

### <span data-ttu-id="eeb03-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="eeb03-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String> [-PrimaryKey <String>]
 [-SecondaryKey <String>] -Rights <PSAccessRights> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eeb03-106">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="eeb03-106">ResourceIdSet</span></span>
```
Add-AzIotHubKey [-HubId] <String> [-KeyName] <String> [-PrimaryKey <String>] [-SecondaryKey <String>]
 -Rights <PSAccessRights> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eeb03-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="eeb03-107">DESCRIPTION</span></span>
<span data-ttu-id="eeb03-108">Erstellt einen Schlüssel für den bereitgestellten IotHub.</span><span class="sxs-lookup"><span data-stu-id="eeb03-108">Creates a Key for the provided IotHub.</span></span>
<span data-ttu-id="eeb03-109">Keynames sind nicht eindeutig und müssen sorgfältig verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="eeb03-109">KeyNames are not unique and need to be managed carefully.</span></span>

## <span data-ttu-id="eeb03-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="eeb03-110">EXAMPLES</span></span>

### <span data-ttu-id="eeb03-111">Beispiel 1 Hinzufügen eines Schlüssels zu einem IotHub</span><span class="sxs-lookup"><span data-stu-id="eeb03-111">Example 1 Add a Key to an IotHub</span></span>
```
PS C:\> Add-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "newkey" -PrimaryKey "primarykey" -SecondaryKey "secondarykey" -Rights RegistryRead
```

<span data-ttu-id="eeb03-112">Erstellt einen Schlüssel mit dem Namen "MyKey" für die iothub "myiothub" mit RegistryRead-Berechtigungen.</span><span class="sxs-lookup"><span data-stu-id="eeb03-112">Creates a key named "mykey" for the iothub "myiothub" with RegistryRead permissions.</span></span>

## <span data-ttu-id="eeb03-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="eeb03-113">PARAMETERS</span></span>

### <span data-ttu-id="eeb03-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eeb03-114">-DefaultProfile</span></span>
<span data-ttu-id="eeb03-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="eeb03-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="eeb03-116">-HubId</span><span class="sxs-lookup"><span data-stu-id="eeb03-116">-HubId</span></span>
<span data-ttu-id="eeb03-117">IotHub-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="eeb03-117">IotHub Resource Id</span></span>

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

### <span data-ttu-id="eeb03-118">-KeyName</span><span class="sxs-lookup"><span data-stu-id="eeb03-118">-KeyName</span></span>
<span data-ttu-id="eeb03-119">Name des Schlüssels</span><span class="sxs-lookup"><span data-stu-id="eeb03-119">Name of the Key</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eeb03-120">-Name</span><span class="sxs-lookup"><span data-stu-id="eeb03-120">-Name</span></span>
<span data-ttu-id="eeb03-121">Name des IotHub</span><span class="sxs-lookup"><span data-stu-id="eeb03-121">Name of the IotHub</span></span>

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

### <span data-ttu-id="eeb03-122">-Primär Primär</span><span class="sxs-lookup"><span data-stu-id="eeb03-122">-PrimaryKey</span></span>
<span data-ttu-id="eeb03-123">Der Primärschlüssel</span><span class="sxs-lookup"><span data-stu-id="eeb03-123">The primary key</span></span>

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

### <span data-ttu-id="eeb03-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eeb03-124">-ResourceGroupName</span></span>
<span data-ttu-id="eeb03-125">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="eeb03-125">Resource Group Name</span></span>

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

### <span data-ttu-id="eeb03-126">-Rechte</span><span class="sxs-lookup"><span data-stu-id="eeb03-126">-Rights</span></span>
<span data-ttu-id="eeb03-127">Die Berechtigungen für diesen IOTHub</span><span class="sxs-lookup"><span data-stu-id="eeb03-127">The permissions for this IOTHub</span></span>

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

### <span data-ttu-id="eeb03-128">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="eeb03-128">-SecondaryKey</span></span>
<span data-ttu-id="eeb03-129">Der sekundäre Schlüssel</span><span class="sxs-lookup"><span data-stu-id="eeb03-129">The Secondary Key</span></span>

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

### <span data-ttu-id="eeb03-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="eeb03-130">-Confirm</span></span>
<span data-ttu-id="eeb03-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="eeb03-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eeb03-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eeb03-132">-WhatIf</span></span>
<span data-ttu-id="eeb03-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="eeb03-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eeb03-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="eeb03-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eeb03-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eeb03-135">CommonParameters</span></span>
<span data-ttu-id="eeb03-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eeb03-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eeb03-137">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eeb03-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eeb03-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="eeb03-138">INPUTS</span></span>

### <span data-ttu-id="eeb03-139">System. String</span><span class="sxs-lookup"><span data-stu-id="eeb03-139">System.String</span></span>

## <span data-ttu-id="eeb03-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="eeb03-140">OUTPUTS</span></span>

### <span data-ttu-id="eeb03-141">Microsoft. Azure. Commands. Management. IotHub. Models. PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="eeb03-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="eeb03-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="eeb03-142">NOTES</span></span>

## <span data-ttu-id="eeb03-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="eeb03-143">RELATED LINKS</span></span>
