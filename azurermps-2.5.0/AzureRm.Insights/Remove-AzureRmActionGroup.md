---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 8D8FE2FE-03E7-453E-B968-E28B07E42EF2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/remove-azurermactiongroup
schema: 2.0.0
ms.openlocfilehash: 7ec50b0698017c20fb47030ccb571d6b4083b97b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849323"
---
# <span data-ttu-id="9c26a-101">Remove-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="9c26a-101">Remove-AzureRmActionGroup</span></span>

## <span data-ttu-id="9c26a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9c26a-102">SYNOPSIS</span></span>
<span data-ttu-id="9c26a-103">Entfernt eine Aktionsgruppe.</span><span class="sxs-lookup"><span data-stu-id="9c26a-103">Removes an action group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9c26a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9c26a-104">SYNTAX</span></span>

### <span data-ttu-id="9c26a-105">ByPropertyName (Standard)</span><span class="sxs-lookup"><span data-stu-id="9c26a-105">ByPropertyName (Default)</span></span>
```
Remove-AzureRmActionGroup -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9c26a-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="9c26a-106">ByResourceId</span></span>
```
Remove-AzureRmActionGroup -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9c26a-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="9c26a-107">ByInputObject</span></span>
```
Remove-AzureRmActionGroup -InputObject <PSActionGroupResource> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9c26a-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9c26a-108">DESCRIPTION</span></span>
<span data-ttu-id="9c26a-109">Das Cmdlet **Remove-AzureRmActionGroup** entfernt eine Aktionsgruppe.</span><span class="sxs-lookup"><span data-stu-id="9c26a-109">The **Remove-AzureRmActionGroup** cmdlet removes an action group.</span></span>

## <span data-ttu-id="9c26a-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9c26a-110">EXAMPLES</span></span>

### <span data-ttu-id="9c26a-111">Beispiel 1: Entfernen einer Aktionsgruppe</span><span class="sxs-lookup"><span data-stu-id="9c26a-111">Example 1: Remove an action group</span></span>
```
PS C:\>Remove-AzureRmActionGroup -ResourceGroup "Default-Web-CentralUS" -Name "myActionGroup"
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
2c6c159b-0e73-4a01-a67b-c32c1a0008a3                                                                                 OK
```

## <span data-ttu-id="9c26a-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="9c26a-112">PARAMETERS</span></span>

### <span data-ttu-id="9c26a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c26a-113">-DefaultProfile</span></span>
<span data-ttu-id="9c26a-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="9c26a-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9c26a-115">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="9c26a-115">-InputObject</span></span>
<span data-ttu-id="9c26a-116">Aktionsgruppe resourc</span><span class="sxs-lookup"><span data-stu-id="9c26a-116">The action group resourc</span></span>

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

### <span data-ttu-id="9c26a-117">-Name</span><span class="sxs-lookup"><span data-stu-id="9c26a-117">-Name</span></span>
<span data-ttu-id="9c26a-118">Der Name der Aktionsgruppe.</span><span class="sxs-lookup"><span data-stu-id="9c26a-118">The name of the action group.</span></span>

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

### <span data-ttu-id="9c26a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c26a-119">-ResourceGroupName</span></span>
<span data-ttu-id="9c26a-120">Die Ressourcengruppe Nam</span><span class="sxs-lookup"><span data-stu-id="9c26a-120">The resource group nam</span></span>

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

### <span data-ttu-id="9c26a-121">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="9c26a-121">-ResourceId</span></span>
<span data-ttu-id="9c26a-122">Die Ressource i</span><span class="sxs-lookup"><span data-stu-id="9c26a-122">The resource i</span></span>

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

### <span data-ttu-id="9c26a-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9c26a-123">-Confirm</span></span>
<span data-ttu-id="9c26a-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9c26a-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9c26a-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9c26a-125">-WhatIf</span></span>
<span data-ttu-id="9c26a-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9c26a-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9c26a-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9c26a-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9c26a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c26a-128">CommonParameters</span></span>
<span data-ttu-id="9c26a-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c26a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c26a-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c26a-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c26a-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9c26a-131">INPUTS</span></span>

### <span data-ttu-id="9c26a-132">System. String</span><span class="sxs-lookup"><span data-stu-id="9c26a-132">System.String</span></span>

### <span data-ttu-id="9c26a-133">Microsoft. Azure. Commands. Insights. OutputClasses. PSActionGroupResource</span><span class="sxs-lookup"><span data-stu-id="9c26a-133">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span></span>
<span data-ttu-id="9c26a-134">Parameter: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="9c26a-134">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="9c26a-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9c26a-135">OUTPUTS</span></span>

### <span data-ttu-id="9c26a-136">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="9c26a-136">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="9c26a-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="9c26a-137">NOTES</span></span>

## <span data-ttu-id="9c26a-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9c26a-138">RELATED LINKS</span></span>

<span data-ttu-id="9c26a-139">[Satz-AzureRmActionGroup](./Set-AzureRmActionGroup.md) 
 [Get-AzureRmActionGroup](./Get-AzureRmActionGroup.md) 
 [Neu – AzureRmActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span><span class="sxs-lookup"><span data-stu-id="9c26a-139">[Set-AzureRmActionGroup](./Set-AzureRmActionGroup.md)
[Get-AzureRmActionGroup](./Get-AzureRmActionGroup.md)
[New-AzureRmActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span></span>
