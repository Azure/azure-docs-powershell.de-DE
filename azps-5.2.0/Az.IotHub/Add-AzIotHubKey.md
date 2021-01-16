---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubKey.md
ms.openlocfilehash: 422eb25456beb57ed6ab029fa5d70a47061ca491
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98299347"
---
# <span data-ttu-id="acf77-101">Add-AzIotHubKey</span><span class="sxs-lookup"><span data-stu-id="acf77-101">Add-AzIotHubKey</span></span>

## <span data-ttu-id="acf77-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="acf77-102">SYNOPSIS</span></span>
<span data-ttu-id="acf77-103">Erstellt einen IotHub-Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="acf77-103">Creates an IotHub Key.</span></span>

## <span data-ttu-id="acf77-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="acf77-104">SYNTAX</span></span>

### <span data-ttu-id="acf77-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="acf77-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String> [-PrimaryKey <String>]
 [-SecondaryKey <String>] -Rights <PSAccessRights> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="acf77-106">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="acf77-106">ResourceIdSet</span></span>
```
Add-AzIotHubKey [-HubId] <String> [-KeyName] <String> [-PrimaryKey <String>] [-SecondaryKey <String>]
 -Rights <PSAccessRights> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="acf77-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="acf77-107">DESCRIPTION</span></span>
<span data-ttu-id="acf77-108">Erstellt einen Schlüssel für den bereitgestellten IotHub.</span><span class="sxs-lookup"><span data-stu-id="acf77-108">Creates a Key for the provided IotHub.</span></span>
<span data-ttu-id="acf77-109">KeyNames sind nicht eindeutig und müssen sorgfältig verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="acf77-109">KeyNames are not unique and need to be managed carefully.</span></span>

## <span data-ttu-id="acf77-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="acf77-110">EXAMPLES</span></span>

### <span data-ttu-id="acf77-111">Beispiel 1 Hinzufügen eines Schlüssels zu einem IotHub</span><span class="sxs-lookup"><span data-stu-id="acf77-111">Example 1 Add a Key to an IotHub</span></span>
```
PS C:\> Add-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "newkey" -PrimaryKey "primarykey" -SecondaryKey "secondarykey" -Rights RegistryRead
```

<span data-ttu-id="acf77-112">Erstellt einen Schlüssel mit dem Namen "mykey" für den iothub "myiothub" mit RegistryRead-Berechtigungen.</span><span class="sxs-lookup"><span data-stu-id="acf77-112">Creates a key named "mykey" for the iothub "myiothub" with RegistryRead permissions.</span></span>

## <span data-ttu-id="acf77-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="acf77-113">PARAMETERS</span></span>

### <span data-ttu-id="acf77-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="acf77-114">-DefaultProfile</span></span>
<span data-ttu-id="acf77-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="acf77-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="acf77-116">-HubId</span><span class="sxs-lookup"><span data-stu-id="acf77-116">-HubId</span></span>
<span data-ttu-id="acf77-117">IotHub-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="acf77-117">IotHub Resource Id</span></span>

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

### <span data-ttu-id="acf77-118">-KeyName</span><span class="sxs-lookup"><span data-stu-id="acf77-118">-KeyName</span></span>
<span data-ttu-id="acf77-119">Name des Schlüssels</span><span class="sxs-lookup"><span data-stu-id="acf77-119">Name of the Key</span></span>

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

### <span data-ttu-id="acf77-120">-Name</span><span class="sxs-lookup"><span data-stu-id="acf77-120">-Name</span></span>
<span data-ttu-id="acf77-121">Name des IotHub</span><span class="sxs-lookup"><span data-stu-id="acf77-121">Name of the IotHub</span></span>

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

### <span data-ttu-id="acf77-122">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="acf77-122">-PrimaryKey</span></span>
<span data-ttu-id="acf77-123">Der Primärschlüssel</span><span class="sxs-lookup"><span data-stu-id="acf77-123">The primary key</span></span>

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

### <span data-ttu-id="acf77-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="acf77-124">-ResourceGroupName</span></span>
<span data-ttu-id="acf77-125">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="acf77-125">Resource Group Name</span></span>

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

### <span data-ttu-id="acf77-126">-Rights</span><span class="sxs-lookup"><span data-stu-id="acf77-126">-Rights</span></span>
<span data-ttu-id="acf77-127">Die Berechtigungen für diesen IOTHub</span><span class="sxs-lookup"><span data-stu-id="acf77-127">The permissions for this IOTHub</span></span>

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

### <span data-ttu-id="acf77-128">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="acf77-128">-SecondaryKey</span></span>
<span data-ttu-id="acf77-129">Der sekundäre Schlüssel</span><span class="sxs-lookup"><span data-stu-id="acf77-129">The Secondary Key</span></span>

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

### <span data-ttu-id="acf77-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="acf77-130">-Confirm</span></span>
<span data-ttu-id="acf77-131">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="acf77-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="acf77-132">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="acf77-132">-WhatIf</span></span>
<span data-ttu-id="acf77-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="acf77-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="acf77-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="acf77-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="acf77-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="acf77-135">CommonParameters</span></span>
<span data-ttu-id="acf77-136">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="acf77-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="acf77-137">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="acf77-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="acf77-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="acf77-138">INPUTS</span></span>

### <span data-ttu-id="acf77-139">System.String</span><span class="sxs-lookup"><span data-stu-id="acf77-139">System.String</span></span>

## <span data-ttu-id="acf77-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="acf77-140">OUTPUTS</span></span>

### <span data-ttu-id="acf77-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="acf77-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="acf77-142">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="acf77-142">NOTES</span></span>

## <span data-ttu-id="acf77-143">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="acf77-143">RELATED LINKS</span></span>
