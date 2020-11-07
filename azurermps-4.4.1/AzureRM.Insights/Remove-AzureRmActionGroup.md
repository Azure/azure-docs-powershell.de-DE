---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 8D8FE2FE-03E7-453E-B968-E28B07E42EF2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmActionGroup.md
ms.openlocfilehash: 0b5f84a38fcd087b77b32624b9cbd9b3b8a27e05
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664763"
---
# <span data-ttu-id="64985-101">Remove-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="64985-101">Remove-AzureRmActionGroup</span></span>

## <span data-ttu-id="64985-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="64985-102">SYNOPSIS</span></span>
<span data-ttu-id="64985-103">Entfernt eine Aktionsgruppe.</span><span class="sxs-lookup"><span data-stu-id="64985-103">Removes an action group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="64985-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="64985-104">SYNTAX</span></span>

### <span data-ttu-id="64985-105">ByPropertyName (Standard)</span><span class="sxs-lookup"><span data-stu-id="64985-105">ByPropertyName (Default)</span></span>
```
Remove-AzureRmActionGroup -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="64985-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="64985-106">ByResourceId</span></span>
```
Remove-AzureRmActionGroup -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="64985-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="64985-107">ByInputObject</span></span>
```
Remove-AzureRmActionGroup -InputObject <PSActionGroupResource> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="64985-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="64985-108">DESCRIPTION</span></span>
<span data-ttu-id="64985-109">Das Cmdlet **Remove-AzureRmActionGroup** entfernt eine Aktionsgruppe.</span><span class="sxs-lookup"><span data-stu-id="64985-109">The **Remove-AzureRmActionGroup** cmdlet removes an action group.</span></span>

## <span data-ttu-id="64985-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="64985-110">EXAMPLES</span></span>

### <span data-ttu-id="64985-111">Beispiel 1: Entfernen einer Aktionsgruppe</span><span class="sxs-lookup"><span data-stu-id="64985-111">Example 1: Remove an action group</span></span>
```
PS C:\>Remove-AzureRmActionGroup -ResourceGroup "Default-Web-CentralUS" -Name "myActionGroup"
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
2c6c159b-0e73-4a01-a67b-c32c1a0008a3                                                                                 OK
```

## <span data-ttu-id="64985-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="64985-112">PARAMETERS</span></span>

### <span data-ttu-id="64985-113">-Name</span><span class="sxs-lookup"><span data-stu-id="64985-113">-Name</span></span>
<span data-ttu-id="64985-114">Der Name der Aktionsgruppe.</span><span class="sxs-lookup"><span data-stu-id="64985-114">The name of the action group.</span></span>

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

### <span data-ttu-id="64985-115">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="64985-115">-Confirm</span></span>
<span data-ttu-id="64985-116">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="64985-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="64985-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64985-117">-DefaultProfile</span></span>
<span data-ttu-id="64985-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="64985-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="64985-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="64985-119">-InputObject</span></span>
<span data-ttu-id="64985-120">Die Ressource der Aktionsgruppe</span><span class="sxs-lookup"><span data-stu-id="64985-120">The action group resource</span></span>

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

### <span data-ttu-id="64985-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64985-121">-ResourceGroupName</span></span>
<span data-ttu-id="64985-122">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="64985-122">The resource group name</span></span>

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

### <span data-ttu-id="64985-123">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="64985-123">-ResourceId</span></span>
<span data-ttu-id="64985-124">Die Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="64985-124">The resource id</span></span>

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

### <span data-ttu-id="64985-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64985-125">-WhatIf</span></span>
<span data-ttu-id="64985-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="64985-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="64985-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="64985-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="64985-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64985-128">CommonParameters</span></span>
<span data-ttu-id="64985-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64985-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64985-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64985-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64985-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="64985-131">INPUTS</span></span>

## <span data-ttu-id="64985-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="64985-132">OUTPUTS</span></span>

### <span data-ttu-id="64985-133">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="64985-133">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="64985-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="64985-134">NOTES</span></span>

## <span data-ttu-id="64985-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="64985-135">RELATED LINKS</span></span>

<span data-ttu-id="64985-136">[Satz-AzureRmActionGroup](./Set-AzureRmActionGroup.md) 
 [Get-AzureRmActionGroup](./Get-AzureRmActionGroup.md) 
 [Neu – AzureRmActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span><span class="sxs-lookup"><span data-stu-id="64985-136">[Set-AzureRmActionGroup](./Set-AzureRmActionGroup.md)
[Get-AzureRmActionGroup](./Get-AzureRmActionGroup.md)
[New-AzureRmActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span></span>
