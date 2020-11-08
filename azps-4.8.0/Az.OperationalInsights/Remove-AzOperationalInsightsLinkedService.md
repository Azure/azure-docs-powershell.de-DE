---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/remove-azoperationalinsightslinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsLinkedService.md
ms.openlocfilehash: c62dcefc2a4cfabc908c45454f3907c2da060f6c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94165080"
---
# <span data-ttu-id="5ea71-101">Remove-AzOperationalInsightsLinkedService</span><span class="sxs-lookup"><span data-stu-id="5ea71-101">Remove-AzOperationalInsightsLinkedService</span></span>

## <span data-ttu-id="5ea71-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5ea71-102">SYNOPSIS</span></span>
<span data-ttu-id="5ea71-103">Dienst für Arbeitsbereich aufheben</span><span class="sxs-lookup"><span data-stu-id="5ea71-103">Unlink service for workspace</span></span>

## <span data-ttu-id="5ea71-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5ea71-104">SYNTAX</span></span>

```
Remove-AzOperationalInsightsLinkedService [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-LinkedServiceName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5ea71-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5ea71-105">DESCRIPTION</span></span>
<span data-ttu-id="5ea71-106">Dienst für Arbeitsbereich aufheben</span><span class="sxs-lookup"><span data-stu-id="5ea71-106">Unlink service for workspace</span></span>

## <span data-ttu-id="5ea71-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5ea71-107">EXAMPLES</span></span>

### <span data-ttu-id="5ea71-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="5ea71-108">Example 1</span></span>
```powershell
Remove-AzOperationalInsightsLinkedService -ResourceGroupName {rg-name} -WorkspaceName {workspace-name} -LinkedServiceName cluster

true
```

<span data-ttu-id="5ea71-109">Verknüpfungsdienst für Arbeitsbereich aufheben</span><span class="sxs-lookup"><span data-stu-id="5ea71-109">Unlink linked service for workspace</span></span>

## <span data-ttu-id="5ea71-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="5ea71-110">PARAMETERS</span></span>

### <span data-ttu-id="5ea71-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5ea71-111">-AsJob</span></span>
<span data-ttu-id="5ea71-112">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="5ea71-112">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ea71-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ea71-113">-DefaultProfile</span></span>
<span data-ttu-id="5ea71-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5ea71-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ea71-115">-LinkedServiceName</span><span class="sxs-lookup"><span data-stu-id="5ea71-115">-LinkedServiceName</span></span>
<span data-ttu-id="5ea71-116">Der Arbeitsbereichsname.</span><span class="sxs-lookup"><span data-stu-id="5ea71-116">The Workspace name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ea71-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ea71-117">-ResourceGroupName</span></span>
<span data-ttu-id="5ea71-118">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="5ea71-118">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ea71-119">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="5ea71-119">-WorkspaceName</span></span>
<span data-ttu-id="5ea71-120">Der Arbeitsbereichsname.</span><span class="sxs-lookup"><span data-stu-id="5ea71-120">The Workspace name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ea71-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5ea71-121">-Confirm</span></span>
<span data-ttu-id="5ea71-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5ea71-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ea71-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ea71-123">-WhatIf</span></span>
<span data-ttu-id="5ea71-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5ea71-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5ea71-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5ea71-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ea71-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ea71-126">CommonParameters</span></span>
<span data-ttu-id="5ea71-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ea71-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ea71-128">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5ea71-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ea71-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5ea71-129">INPUTS</span></span>

### <span data-ttu-id="5ea71-130">System. String</span><span class="sxs-lookup"><span data-stu-id="5ea71-130">System.String</span></span>

## <span data-ttu-id="5ea71-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5ea71-131">OUTPUTS</span></span>

### <span data-ttu-id="5ea71-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5ea71-132">System.Boolean</span></span>

## <span data-ttu-id="5ea71-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="5ea71-133">NOTES</span></span>

## <span data-ttu-id="5ea71-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5ea71-134">RELATED LINKS</span></span>
