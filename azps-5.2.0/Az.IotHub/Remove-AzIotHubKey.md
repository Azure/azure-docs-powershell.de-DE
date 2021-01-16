---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubKey.md
ms.openlocfilehash: c50ee56a5dcb15c3b199e9aaf08aeca74828cc66
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98293183"
---
# <span data-ttu-id="7ee3e-101">Remove-AzIotHubKey</span><span class="sxs-lookup"><span data-stu-id="7ee3e-101">Remove-AzIotHubKey</span></span>

## <span data-ttu-id="7ee3e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7ee3e-102">SYNOPSIS</span></span>
<span data-ttu-id="7ee3e-103">Entfernt einen IotHub-Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="7ee3e-103">Removes an IotHub Key.</span></span>

## <span data-ttu-id="7ee3e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7ee3e-104">SYNTAX</span></span>

### <span data-ttu-id="7ee3e-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="7ee3e-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7ee3e-106">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="7ee3e-106">ResourceIdSet</span></span>
```
Remove-AzIotHubKey [-HubId] <String> [-KeyName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7ee3e-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7ee3e-107">DESCRIPTION</span></span>
<span data-ttu-id="7ee3e-108">Entfernt einen IotHub-Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="7ee3e-108">Removes an IotHub Key.</span></span>
<span data-ttu-id="7ee3e-109">Wenn mehrere Schlüssel mit demselben Namen vorhanden sind, wird der erste Schlüssel aus der Liste entfernt.</span><span class="sxs-lookup"><span data-stu-id="7ee3e-109">If there are multiple keys with the same name the first one in the list is removed.</span></span>

## <span data-ttu-id="7ee3e-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="7ee3e-110">EXAMPLES</span></span>

### <span data-ttu-id="7ee3e-111">Beispiel 1 Löschen eines IotHub</span><span class="sxs-lookup"><span data-stu-id="7ee3e-111">Example 1 Delete an IotHub</span></span>
```
PS C:\> Remove-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "iothubowner1"
```

<span data-ttu-id="7ee3e-112">Entfernt den Schlüssel namens "iothubowner1" aus dem IotHub namens "myiothub".</span><span class="sxs-lookup"><span data-stu-id="7ee3e-112">Removes the key named iothubowner1 from the IotHub named "myiothub"</span></span>

## <span data-ttu-id="7ee3e-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7ee3e-113">PARAMETERS</span></span>

### <span data-ttu-id="7ee3e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ee3e-114">-DefaultProfile</span></span>
<span data-ttu-id="7ee3e-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="7ee3e-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7ee3e-116">-HubId</span><span class="sxs-lookup"><span data-stu-id="7ee3e-116">-HubId</span></span>
<span data-ttu-id="7ee3e-117">IotHub-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="7ee3e-117">IotHub Resource Id</span></span>

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

### <span data-ttu-id="7ee3e-118">-KeyName</span><span class="sxs-lookup"><span data-stu-id="7ee3e-118">-KeyName</span></span>
<span data-ttu-id="7ee3e-119">Name des Schlüssels</span><span class="sxs-lookup"><span data-stu-id="7ee3e-119">Name of the Key</span></span>

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

### <span data-ttu-id="7ee3e-120">-Name</span><span class="sxs-lookup"><span data-stu-id="7ee3e-120">-Name</span></span>
<span data-ttu-id="7ee3e-121">Name des IotHub</span><span class="sxs-lookup"><span data-stu-id="7ee3e-121">Name of the IotHub</span></span>

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

### <span data-ttu-id="7ee3e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ee3e-122">-ResourceGroupName</span></span>
<span data-ttu-id="7ee3e-123">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="7ee3e-123">Resource Group Name</span></span>

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

### <span data-ttu-id="7ee3e-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7ee3e-124">-Confirm</span></span>
<span data-ttu-id="7ee3e-125">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7ee3e-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7ee3e-126">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="7ee3e-126">-WhatIf</span></span>
<span data-ttu-id="7ee3e-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7ee3e-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7ee3e-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7ee3e-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7ee3e-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ee3e-129">CommonParameters</span></span>
<span data-ttu-id="7ee3e-130">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ee3e-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ee3e-131">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ee3e-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ee3e-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="7ee3e-132">INPUTS</span></span>

### <span data-ttu-id="7ee3e-133">System.String</span><span class="sxs-lookup"><span data-stu-id="7ee3e-133">System.String</span></span>

## <span data-ttu-id="7ee3e-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="7ee3e-134">OUTPUTS</span></span>

### <span data-ttu-id="7ee3e-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="7ee3e-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="7ee3e-136">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="7ee3e-136">NOTES</span></span>

## <span data-ttu-id="7ee3e-137">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="7ee3e-137">RELATED LINKS</span></span>
