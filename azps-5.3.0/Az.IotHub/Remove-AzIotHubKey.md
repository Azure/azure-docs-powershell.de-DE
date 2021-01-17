---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubKey.md
ms.openlocfilehash: c50ee56a5dcb15c3b199e9aaf08aeca74828cc66
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98386685"
---
# <span data-ttu-id="b5117-101">Remove-AzIotHubKey</span><span class="sxs-lookup"><span data-stu-id="b5117-101">Remove-AzIotHubKey</span></span>

## <span data-ttu-id="b5117-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b5117-102">SYNOPSIS</span></span>
<span data-ttu-id="b5117-103">Entfernt einen IotHub-Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="b5117-103">Removes an IotHub Key.</span></span>

## <span data-ttu-id="b5117-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b5117-104">SYNTAX</span></span>

### <span data-ttu-id="b5117-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="b5117-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b5117-106">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="b5117-106">ResourceIdSet</span></span>
```
Remove-AzIotHubKey [-HubId] <String> [-KeyName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b5117-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b5117-107">DESCRIPTION</span></span>
<span data-ttu-id="b5117-108">Entfernt einen IotHub-Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="b5117-108">Removes an IotHub Key.</span></span>
<span data-ttu-id="b5117-109">Wenn mehrere Schlüssel mit demselben Namen vorhanden sind, wird der erste Schlüssel aus der Liste entfernt.</span><span class="sxs-lookup"><span data-stu-id="b5117-109">If there are multiple keys with the same name the first one in the list is removed.</span></span>

## <span data-ttu-id="b5117-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b5117-110">EXAMPLES</span></span>

### <span data-ttu-id="b5117-111">Beispiel 1 Löschen eines IotHub</span><span class="sxs-lookup"><span data-stu-id="b5117-111">Example 1 Delete an IotHub</span></span>
```
PS C:\> Remove-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "iothubowner1"
```

<span data-ttu-id="b5117-112">Entfernt den Schlüssel namens "iothubowner1" aus dem IotHub namens "myiothub".</span><span class="sxs-lookup"><span data-stu-id="b5117-112">Removes the key named iothubowner1 from the IotHub named "myiothub"</span></span>

## <span data-ttu-id="b5117-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b5117-113">PARAMETERS</span></span>

### <span data-ttu-id="b5117-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5117-114">-DefaultProfile</span></span>
<span data-ttu-id="b5117-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="b5117-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b5117-116">-HubId</span><span class="sxs-lookup"><span data-stu-id="b5117-116">-HubId</span></span>
<span data-ttu-id="b5117-117">IotHub-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="b5117-117">IotHub Resource Id</span></span>

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

### <span data-ttu-id="b5117-118">-KeyName</span><span class="sxs-lookup"><span data-stu-id="b5117-118">-KeyName</span></span>
<span data-ttu-id="b5117-119">Name des Schlüssels</span><span class="sxs-lookup"><span data-stu-id="b5117-119">Name of the Key</span></span>

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

### <span data-ttu-id="b5117-120">-Name</span><span class="sxs-lookup"><span data-stu-id="b5117-120">-Name</span></span>
<span data-ttu-id="b5117-121">Name des IotHub</span><span class="sxs-lookup"><span data-stu-id="b5117-121">Name of the IotHub</span></span>

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

### <span data-ttu-id="b5117-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5117-122">-ResourceGroupName</span></span>
<span data-ttu-id="b5117-123">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="b5117-123">Resource Group Name</span></span>

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

### <span data-ttu-id="b5117-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b5117-124">-Confirm</span></span>
<span data-ttu-id="b5117-125">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b5117-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b5117-126">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="b5117-126">-WhatIf</span></span>
<span data-ttu-id="b5117-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b5117-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b5117-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b5117-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b5117-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5117-129">CommonParameters</span></span>
<span data-ttu-id="b5117-130">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5117-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5117-131">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5117-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5117-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b5117-132">INPUTS</span></span>

### <span data-ttu-id="b5117-133">System.String</span><span class="sxs-lookup"><span data-stu-id="b5117-133">System.String</span></span>

## <span data-ttu-id="b5117-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b5117-134">OUTPUTS</span></span>

### <span data-ttu-id="b5117-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="b5117-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="b5117-136">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="b5117-136">NOTES</span></span>

## <span data-ttu-id="b5117-137">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="b5117-137">RELATED LINKS</span></span>
