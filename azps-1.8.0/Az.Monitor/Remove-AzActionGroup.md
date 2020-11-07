---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 8D8FE2FE-03E7-453E-B968-E28B07E42EF2
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azactiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzActionGroup.md
ms.openlocfilehash: dc32d17a887c4a8c9cfd15f952c1d411a8ef1700
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93661010"
---
# <span data-ttu-id="72dcf-101">Remove-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="72dcf-101">Remove-AzActionGroup</span></span>

## <span data-ttu-id="72dcf-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="72dcf-102">SYNOPSIS</span></span>
<span data-ttu-id="72dcf-103">Entfernt eine Aktionsgruppe.</span><span class="sxs-lookup"><span data-stu-id="72dcf-103">Removes an action group.</span></span>

## <span data-ttu-id="72dcf-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="72dcf-104">SYNTAX</span></span>

### <span data-ttu-id="72dcf-105">ByPropertyName (Standard)</span><span class="sxs-lookup"><span data-stu-id="72dcf-105">ByPropertyName (Default)</span></span>
```
Remove-AzActionGroup -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="72dcf-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="72dcf-106">ByResourceId</span></span>
```
Remove-AzActionGroup -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="72dcf-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="72dcf-107">ByInputObject</span></span>
```
Remove-AzActionGroup -InputObject <PSActionGroupResource> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="72dcf-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="72dcf-108">DESCRIPTION</span></span>
<span data-ttu-id="72dcf-109">Das Cmdlet **Remove-AzActionGroup** entfernt eine Aktionsgruppe.</span><span class="sxs-lookup"><span data-stu-id="72dcf-109">The **Remove-AzActionGroup** cmdlet removes an action group.</span></span>

## <span data-ttu-id="72dcf-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="72dcf-110">EXAMPLES</span></span>

### <span data-ttu-id="72dcf-111">Beispiel 1: Entfernen einer Aktionsgruppe</span><span class="sxs-lookup"><span data-stu-id="72dcf-111">Example 1: Remove an action group</span></span>
```
PS C:\>Remove-AzActionGroup -ResourceGroup "Default-Web-CentralUS" -Name "myActionGroup"
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
2c6c159b-0e73-4a01-a67b-c32c1a0008a3                                                                                 OK
```

## <span data-ttu-id="72dcf-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="72dcf-112">PARAMETERS</span></span>

### <span data-ttu-id="72dcf-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72dcf-113">-DefaultProfile</span></span>
<span data-ttu-id="72dcf-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="72dcf-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="72dcf-115">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="72dcf-115">-InputObject</span></span>
<span data-ttu-id="72dcf-116">Aktionsgruppe resourc</span><span class="sxs-lookup"><span data-stu-id="72dcf-116">The action group resourc</span></span>

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

### <span data-ttu-id="72dcf-117">-Name</span><span class="sxs-lookup"><span data-stu-id="72dcf-117">-Name</span></span>
<span data-ttu-id="72dcf-118">Der Name der Aktionsgruppe.</span><span class="sxs-lookup"><span data-stu-id="72dcf-118">The name of the action group.</span></span>

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

### <span data-ttu-id="72dcf-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72dcf-119">-ResourceGroupName</span></span>
<span data-ttu-id="72dcf-120">Die Ressourcengruppe Nam</span><span class="sxs-lookup"><span data-stu-id="72dcf-120">The resource group nam</span></span>

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

### <span data-ttu-id="72dcf-121">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="72dcf-121">-ResourceId</span></span>
<span data-ttu-id="72dcf-122">Die Ressource i</span><span class="sxs-lookup"><span data-stu-id="72dcf-122">The resource i</span></span>

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

### <span data-ttu-id="72dcf-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="72dcf-123">-Confirm</span></span>
<span data-ttu-id="72dcf-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="72dcf-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="72dcf-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72dcf-125">-WhatIf</span></span>
<span data-ttu-id="72dcf-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="72dcf-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="72dcf-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="72dcf-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="72dcf-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72dcf-128">CommonParameters</span></span>
<span data-ttu-id="72dcf-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72dcf-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72dcf-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72dcf-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72dcf-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="72dcf-131">INPUTS</span></span>

### <span data-ttu-id="72dcf-132">System. String</span><span class="sxs-lookup"><span data-stu-id="72dcf-132">System.String</span></span>

### <span data-ttu-id="72dcf-133">Microsoft. Azure. Commands. Insights. OutputClasses. PSActionGroupResource</span><span class="sxs-lookup"><span data-stu-id="72dcf-133">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span></span>

## <span data-ttu-id="72dcf-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="72dcf-134">OUTPUTS</span></span>

### <span data-ttu-id="72dcf-135">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="72dcf-135">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="72dcf-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="72dcf-136">NOTES</span></span>

## <span data-ttu-id="72dcf-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="72dcf-137">RELATED LINKS</span></span>

<span data-ttu-id="72dcf-138">[Satz-AzActionGroup](./Set-AzActionGroup.md) 
 [Get-AzActionGroup](./Get-AzActionGroup.md) 
 [Neu – AzActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span><span class="sxs-lookup"><span data-stu-id="72dcf-138">[Set-AzActionGroup](./Set-AzActionGroup.md)
[Get-AzActionGroup](./Get-AzActionGroup.md)
[New-AzActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span></span>
