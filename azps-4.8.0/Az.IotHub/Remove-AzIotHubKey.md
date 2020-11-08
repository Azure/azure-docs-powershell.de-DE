---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubKey.md
ms.openlocfilehash: c50ee56a5dcb15c3b199e9aaf08aeca74828cc66
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94010198"
---
# <span data-ttu-id="8623d-101">Remove-AzIotHubKey</span><span class="sxs-lookup"><span data-stu-id="8623d-101">Remove-AzIotHubKey</span></span>

## <span data-ttu-id="8623d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8623d-102">SYNOPSIS</span></span>
<span data-ttu-id="8623d-103">Entfernt einen IotHub-Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="8623d-103">Removes an IotHub Key.</span></span>

## <span data-ttu-id="8623d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8623d-104">SYNTAX</span></span>

### <span data-ttu-id="8623d-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="8623d-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8623d-106">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="8623d-106">ResourceIdSet</span></span>
```
Remove-AzIotHubKey [-HubId] <String> [-KeyName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8623d-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8623d-107">DESCRIPTION</span></span>
<span data-ttu-id="8623d-108">Entfernt einen IotHub-Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="8623d-108">Removes an IotHub Key.</span></span>
<span data-ttu-id="8623d-109">Wenn mehrere Schlüssel mit demselben Namen vorhanden sind, wird der erste in der Liste entfernt.</span><span class="sxs-lookup"><span data-stu-id="8623d-109">If there are multiple keys with the same name the first one in the list is removed.</span></span>

## <span data-ttu-id="8623d-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8623d-110">EXAMPLES</span></span>

### <span data-ttu-id="8623d-111">Beispiel 1 Löschen eines IotHub</span><span class="sxs-lookup"><span data-stu-id="8623d-111">Example 1 Delete an IotHub</span></span>
```
PS C:\> Remove-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "iothubowner1"
```

<span data-ttu-id="8623d-112">Entfernt den Schlüssel mit dem Namen iothubowner1 aus dem IotHub mit dem Namen "myiothub".</span><span class="sxs-lookup"><span data-stu-id="8623d-112">Removes the key named iothubowner1 from the IotHub named "myiothub"</span></span>

## <span data-ttu-id="8623d-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="8623d-113">PARAMETERS</span></span>

### <span data-ttu-id="8623d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8623d-114">-DefaultProfile</span></span>
<span data-ttu-id="8623d-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="8623d-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8623d-116">-HubId</span><span class="sxs-lookup"><span data-stu-id="8623d-116">-HubId</span></span>
<span data-ttu-id="8623d-117">IotHub-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="8623d-117">IotHub Resource Id</span></span>

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

### <span data-ttu-id="8623d-118">-KeyName</span><span class="sxs-lookup"><span data-stu-id="8623d-118">-KeyName</span></span>
<span data-ttu-id="8623d-119">Name des Schlüssels</span><span class="sxs-lookup"><span data-stu-id="8623d-119">Name of the Key</span></span>

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

### <span data-ttu-id="8623d-120">-Name</span><span class="sxs-lookup"><span data-stu-id="8623d-120">-Name</span></span>
<span data-ttu-id="8623d-121">Name des IotHub</span><span class="sxs-lookup"><span data-stu-id="8623d-121">Name of the IotHub</span></span>

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

### <span data-ttu-id="8623d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8623d-122">-ResourceGroupName</span></span>
<span data-ttu-id="8623d-123">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="8623d-123">Resource Group Name</span></span>

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

### <span data-ttu-id="8623d-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8623d-124">-Confirm</span></span>
<span data-ttu-id="8623d-125">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8623d-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8623d-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8623d-126">-WhatIf</span></span>
<span data-ttu-id="8623d-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8623d-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8623d-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8623d-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8623d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8623d-129">CommonParameters</span></span>
<span data-ttu-id="8623d-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8623d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8623d-131">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8623d-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8623d-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8623d-132">INPUTS</span></span>

### <span data-ttu-id="8623d-133">System. String</span><span class="sxs-lookup"><span data-stu-id="8623d-133">System.String</span></span>

## <span data-ttu-id="8623d-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8623d-134">OUTPUTS</span></span>

### <span data-ttu-id="8623d-135">Microsoft. Azure. Commands. Management. IotHub. Models. PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="8623d-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="8623d-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="8623d-136">NOTES</span></span>

## <span data-ttu-id="8623d-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8623d-137">RELATED LINKS</span></span>
