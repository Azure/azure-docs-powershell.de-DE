---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatasharesubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareSubscription.md
ms.openlocfilehash: 12298f5c61981cb34572a104d39a279f7024adf2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94003072"
---
# <span data-ttu-id="13801-101">Remove-AzDataShareSubscription</span><span class="sxs-lookup"><span data-stu-id="13801-101">Remove-AzDataShareSubscription</span></span>

## <span data-ttu-id="13801-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="13801-102">SYNOPSIS</span></span>
<span data-ttu-id="13801-103">entfernt ein Freigabe Abonnement</span><span class="sxs-lookup"><span data-stu-id="13801-103">removes a share subscription</span></span>

## <span data-ttu-id="13801-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="13801-104">SYNTAX</span></span>

### <span data-ttu-id="13801-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="13801-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareSubscription -ResourceGroupName <String> -AccountName <String> -Name <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="13801-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="13801-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareSubscription -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="13801-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="13801-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareSubscription -InputObject <PSDataShareSubscription> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="13801-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="13801-108">DESCRIPTION</span></span>
<span data-ttu-id="13801-109">Das Cmdlet " **Remove-AzDataShareSubscription** " entfernt ein Freigabe Abonnement.</span><span class="sxs-lookup"><span data-stu-id="13801-109">The **Remove-AzDataShareSubscription** cmdlet removes a share subscription</span></span>

## <span data-ttu-id="13801-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="13801-110">EXAMPLES</span></span>

### <span data-ttu-id="13801-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="13801-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareSubscription -ResourceGroupName "ADS" -AccountName "WikiAds" -Name "AdsShareSubscription"
Are you sure you want to remove sharesubscription "AdsShareSubscription"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="13801-112">Mit diesen Befehlen wird ein sharesubscription namens AdsShareSubscription aus dem Konto WikiAds entfernt.</span><span class="sxs-lookup"><span data-stu-id="13801-112">This commands removes a sharesubscription named AdsShareSubscription from account WikiAds.</span></span> 

## <span data-ttu-id="13801-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="13801-113">PARAMETERS</span></span>

### <span data-ttu-id="13801-114">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="13801-114">-AccountName</span></span>
<span data-ttu-id="13801-115">Name des Azure Data Share-Kontos</span><span class="sxs-lookup"><span data-stu-id="13801-115">Azure data share account name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13801-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="13801-116">-AsJob</span></span>
<span data-ttu-id="13801-117">{{Fill AsJob Description}}</span><span class="sxs-lookup"><span data-stu-id="13801-117">{{Fill AsJob Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13801-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13801-118">-DefaultProfile</span></span>
<span data-ttu-id="13801-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="13801-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="13801-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="13801-120">-InputObject</span></span>
<span data-ttu-id="13801-121">Azure Data Share-Abonnementobjekt</span><span class="sxs-lookup"><span data-stu-id="13801-121">Azure data share subscription object</span></span>


```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="13801-122">-Name</span><span class="sxs-lookup"><span data-stu-id="13801-122">-Name</span></span>
<span data-ttu-id="13801-123">Name des Azure Data Share-Abonnements</span><span class="sxs-lookup"><span data-stu-id="13801-123">Azure data share subscription name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13801-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="13801-124">-PassThru</span></span>
<span data-ttu-id="13801-125">Objekt zurückgeben (sofern angegeben).</span><span class="sxs-lookup"><span data-stu-id="13801-125">Return object (if specified).</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13801-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13801-126">-ResourceGroupName</span></span>
<span data-ttu-id="13801-127">Der Name der Ressourcengruppe des Azure Data Share-Kontos</span><span class="sxs-lookup"><span data-stu-id="13801-127">The resource group name of the azure data share account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13801-128">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="13801-128">-ResourceId</span></span>
<span data-ttu-id="13801-129">Die Ressourcen-ID des Azure Data Share-Abonnements</span><span class="sxs-lookup"><span data-stu-id="13801-129">The resource id of the azure data share subscription</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13801-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="13801-130">-Confirm</span></span>
<span data-ttu-id="13801-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="13801-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="13801-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="13801-132">-WhatIf</span></span>
<span data-ttu-id="13801-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="13801-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="13801-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="13801-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="13801-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13801-135">CommonParameters</span></span>
<span data-ttu-id="13801-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13801-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13801-137">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13801-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13801-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="13801-138">INPUTS</span></span>

### <span data-ttu-id="13801-139">System. String</span><span class="sxs-lookup"><span data-stu-id="13801-139">System.String</span></span>

### <span data-ttu-id="13801-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span><span class="sxs-lookup"><span data-stu-id="13801-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span></span>

## <span data-ttu-id="13801-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="13801-141">OUTPUTS</span></span>

### <span data-ttu-id="13801-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="13801-142">System.Boolean</span></span>

## <span data-ttu-id="13801-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="13801-143">NOTES</span></span>

## <span data-ttu-id="13801-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="13801-144">RELATED LINKS</span></span>
