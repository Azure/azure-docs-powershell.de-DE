---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 8D8FE2FE-03E7-453E-B968-E28B07E42EF2
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azactiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzActionGroup.md
ms.openlocfilehash: 297800cd65f6527a36c8bc486a0ee73e84d98339
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93995082"
---
# <span data-ttu-id="ead62-101">Remove-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="ead62-101">Remove-AzActionGroup</span></span>

## <span data-ttu-id="ead62-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ead62-102">SYNOPSIS</span></span>
<span data-ttu-id="ead62-103">Entfernt eine Aktionsgruppe.</span><span class="sxs-lookup"><span data-stu-id="ead62-103">Removes an action group.</span></span>

## <span data-ttu-id="ead62-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ead62-104">SYNTAX</span></span>

### <span data-ttu-id="ead62-105">ByPropertyName (Standard)</span><span class="sxs-lookup"><span data-stu-id="ead62-105">ByPropertyName (Default)</span></span>
```
Remove-AzActionGroup -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ead62-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="ead62-106">ByResourceId</span></span>
```
Remove-AzActionGroup -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ead62-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="ead62-107">ByInputObject</span></span>
```
Remove-AzActionGroup -InputObject <PSActionGroupResource> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ead62-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ead62-108">DESCRIPTION</span></span>
<span data-ttu-id="ead62-109">Das Cmdlet **Remove-AzActionGroup** entfernt eine Aktionsgruppe.</span><span class="sxs-lookup"><span data-stu-id="ead62-109">The **Remove-AzActionGroup** cmdlet removes an action group.</span></span>

## <span data-ttu-id="ead62-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ead62-110">EXAMPLES</span></span>

### <span data-ttu-id="ead62-111">Beispiel 1: Entfernen einer Aktionsgruppe</span><span class="sxs-lookup"><span data-stu-id="ead62-111">Example 1: Remove an action group</span></span>
```
PS C:\>Remove-AzActionGroup -ResourceGroup "Default-Web-CentralUS" -Name "myActionGroup"
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
2c6c159b-0e73-4a01-a67b-c32c1a0008a3                                                                                 OK
```

## <span data-ttu-id="ead62-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="ead62-112">PARAMETERS</span></span>

### <span data-ttu-id="ead62-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ead62-113">-DefaultProfile</span></span>
<span data-ttu-id="ead62-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="ead62-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ead62-115">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="ead62-115">-InputObject</span></span>
<span data-ttu-id="ead62-116">Die Ressource der Aktionsgruppe</span><span class="sxs-lookup"><span data-stu-id="ead62-116">The action group resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ead62-117">-Name</span><span class="sxs-lookup"><span data-stu-id="ead62-117">-Name</span></span>
<span data-ttu-id="ead62-118">Der Name der Aktionsgruppe.</span><span class="sxs-lookup"><span data-stu-id="ead62-118">The name of the action group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByPropertyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ead62-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ead62-119">-ResourceGroupName</span></span>
<span data-ttu-id="ead62-120">Die Ressourcengruppe Nam</span><span class="sxs-lookup"><span data-stu-id="ead62-120">The resource group nam</span></span>

```yaml
Type: System.String
Parameter Sets: ByPropertyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ead62-121">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="ead62-121">-ResourceId</span></span>
<span data-ttu-id="ead62-122">Die Ressource i</span><span class="sxs-lookup"><span data-stu-id="ead62-122">The resource i</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ead62-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ead62-123">-Confirm</span></span>
<span data-ttu-id="ead62-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ead62-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ead62-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ead62-125">-WhatIf</span></span>
<span data-ttu-id="ead62-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ead62-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ead62-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ead62-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ead62-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ead62-128">CommonParameters</span></span>
<span data-ttu-id="ead62-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ead62-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ead62-130">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ead62-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ead62-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ead62-131">INPUTS</span></span>

### <span data-ttu-id="ead62-132">System. String</span><span class="sxs-lookup"><span data-stu-id="ead62-132">System.String</span></span>

### <span data-ttu-id="ead62-133">Microsoft. Azure. Commands. Insights. OutputClasses. PSActionGroupResource</span><span class="sxs-lookup"><span data-stu-id="ead62-133">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span></span>

## <span data-ttu-id="ead62-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ead62-134">OUTPUTS</span></span>

### <span data-ttu-id="ead62-135">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="ead62-135">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="ead62-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="ead62-136">NOTES</span></span>

## <span data-ttu-id="ead62-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ead62-137">RELATED LINKS</span></span>

<span data-ttu-id="ead62-138">[Satz-AzActionGroup](./Set-AzActionGroup.md) 
 [Get-AzActionGroup](./Get-AzActionGroup.md) 
 [Neu – AzActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span><span class="sxs-lookup"><span data-stu-id="ead62-138">[Set-AzActionGroup](./Set-AzActionGroup.md)
[Get-AzActionGroup](./Get-AzActionGroup.md)
[New-AzActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span></span>
