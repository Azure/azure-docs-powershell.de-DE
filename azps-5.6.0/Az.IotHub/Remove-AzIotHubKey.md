---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/remove-aziothubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubKey.md
ms.openlocfilehash: d9a6936dec16f1723c0e74db7958093aca02ce97
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101934360"
---
# <span data-ttu-id="5ebe1-101">Remove-AzIotHubKey</span><span class="sxs-lookup"><span data-stu-id="5ebe1-101">Remove-AzIotHubKey</span></span>

## <span data-ttu-id="5ebe1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5ebe1-102">SYNOPSIS</span></span>
<span data-ttu-id="5ebe1-103">Entfernt einen IotHub-Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="5ebe1-103">Removes an IotHub Key.</span></span>

## <span data-ttu-id="5ebe1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5ebe1-104">SYNTAX</span></span>

### <span data-ttu-id="5ebe1-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="5ebe1-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5ebe1-106">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="5ebe1-106">ResourceIdSet</span></span>
```
Remove-AzIotHubKey [-HubId] <String> [-KeyName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5ebe1-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5ebe1-107">DESCRIPTION</span></span>
<span data-ttu-id="5ebe1-108">Entfernt einen IotHub-Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="5ebe1-108">Removes an IotHub Key.</span></span>
<span data-ttu-id="5ebe1-109">Wenn mehrere Schlüssel mit demselben Namen vorhanden sind, wird der erste Schlüssel in der Liste entfernt.</span><span class="sxs-lookup"><span data-stu-id="5ebe1-109">If there are multiple keys with the same name the first one in the list is removed.</span></span>

## <span data-ttu-id="5ebe1-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5ebe1-110">EXAMPLES</span></span>

### <span data-ttu-id="5ebe1-111">Beispiel 1 Löschen eines IotHub</span><span class="sxs-lookup"><span data-stu-id="5ebe1-111">Example 1 Delete an IotHub</span></span>
```
PS C:\> Remove-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "iothubowner1"
```

<span data-ttu-id="5ebe1-112">Entfernt den Schlüssel mit dem Namen "iothubowner1" aus dem IotHub mit dem Namen "myiothub".</span><span class="sxs-lookup"><span data-stu-id="5ebe1-112">Removes the key named iothubowner1 from the IotHub named "myiothub"</span></span>

## <span data-ttu-id="5ebe1-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="5ebe1-113">PARAMETERS</span></span>

### <span data-ttu-id="5ebe1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ebe1-114">-DefaultProfile</span></span>
<span data-ttu-id="5ebe1-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="5ebe1-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5ebe1-116">-HubId</span><span class="sxs-lookup"><span data-stu-id="5ebe1-116">-HubId</span></span>
<span data-ttu-id="5ebe1-117">IotHub-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="5ebe1-117">IotHub Resource Id</span></span>

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

### <span data-ttu-id="5ebe1-118">-KeyName</span><span class="sxs-lookup"><span data-stu-id="5ebe1-118">-KeyName</span></span>
<span data-ttu-id="5ebe1-119">Name des Schlüssels</span><span class="sxs-lookup"><span data-stu-id="5ebe1-119">Name of the Key</span></span>

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

### <span data-ttu-id="5ebe1-120">-Name</span><span class="sxs-lookup"><span data-stu-id="5ebe1-120">-Name</span></span>
<span data-ttu-id="5ebe1-121">Name des IotHub</span><span class="sxs-lookup"><span data-stu-id="5ebe1-121">Name of the IotHub</span></span>

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

### <span data-ttu-id="5ebe1-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ebe1-122">-ResourceGroupName</span></span>
<span data-ttu-id="5ebe1-123">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="5ebe1-123">Resource Group Name</span></span>

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

### <span data-ttu-id="5ebe1-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5ebe1-124">-Confirm</span></span>
<span data-ttu-id="5ebe1-125">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5ebe1-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5ebe1-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ebe1-126">-WhatIf</span></span>
<span data-ttu-id="5ebe1-127">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5ebe1-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5ebe1-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5ebe1-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5ebe1-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ebe1-129">CommonParameters</span></span>
<span data-ttu-id="5ebe1-130">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ebe1-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ebe1-131">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ebe1-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ebe1-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5ebe1-132">INPUTS</span></span>

### <span data-ttu-id="5ebe1-133">System.String</span><span class="sxs-lookup"><span data-stu-id="5ebe1-133">System.String</span></span>

## <span data-ttu-id="5ebe1-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5ebe1-134">OUTPUTS</span></span>

### <span data-ttu-id="5ebe1-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="5ebe1-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="5ebe1-136">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="5ebe1-136">NOTES</span></span>

## <span data-ttu-id="5ebe1-137">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="5ebe1-137">RELATED LINKS</span></span>
