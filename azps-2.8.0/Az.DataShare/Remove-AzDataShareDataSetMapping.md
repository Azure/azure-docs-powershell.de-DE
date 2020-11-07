---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatasharedatasetmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareDataSetMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareDataSetMapping.md
ms.openlocfilehash: 249f166bcf4dd61d9b8da7cf4d67a2ac20f705ba
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93651394"
---
# <span data-ttu-id="4d37c-101">Remove-AzDataShareDataSetMapping</span><span class="sxs-lookup"><span data-stu-id="4d37c-101">Remove-AzDataShareDataSetMapping</span></span>

## <span data-ttu-id="4d37c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4d37c-102">SYNOPSIS</span></span>
<span data-ttu-id="4d37c-103">Entfernt eine Daten satzzuordnung</span><span class="sxs-lookup"><span data-stu-id="4d37c-103">Removes a dataset mapping</span></span>

## <span data-ttu-id="4d37c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4d37c-104">SYNTAX</span></span>

### <span data-ttu-id="4d37c-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="4d37c-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareDataSetMapping -ResourceGroupName <String> -AccountName <String>
 -ShareSubscriptionName <String> -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4d37c-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4d37c-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareDataSetMapping -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4d37c-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4d37c-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareDataSetMapping -InputObject <PSDataShareDataSetMapping> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4d37c-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4d37c-108">DESCRIPTION</span></span>
<span data-ttu-id="4d37c-109">Das Cmdlet **Remove-AzDataShareDataSetMapping** entfernt eine DataSet-Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="4d37c-109">The **Remove-AzDataShareDataSetMapping** cmdlet removes a dataset mappings.</span></span>

## <span data-ttu-id="4d37c-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4d37c-110">EXAMPLES</span></span>

### <span data-ttu-id="4d37c-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4d37c-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareDataSetMapping -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareSubscriptionName "AdsShareSubscription" -Name "DSM"
Are you sure you want to remove dataset mapping "DSM"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="4d37c-112">Mit diesen Befehlen wird das DataSet DSM aus sharesubscription WikiAds entfernt.</span><span class="sxs-lookup"><span data-stu-id="4d37c-112">This commands removes the dataset named DSM from sharesubscription WikiAds.</span></span> 

## <span data-ttu-id="4d37c-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="4d37c-113">PARAMETERS</span></span>

### <span data-ttu-id="4d37c-114">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="4d37c-114">-AccountName</span></span>
<span data-ttu-id="4d37c-115">Name des Azure-Datenfreigabe Kontos</span><span class="sxs-lookup"><span data-stu-id="4d37c-115">Azure data share account name</span></span>

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

### <span data-ttu-id="4d37c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d37c-116">-DefaultProfile</span></span>
<span data-ttu-id="4d37c-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4d37c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4d37c-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="4d37c-118">-InputObject</span></span>
<span data-ttu-id="4d37c-119">Das Azure-Daten Satz-Zuordnungsobjekt</span><span class="sxs-lookup"><span data-stu-id="4d37c-119">The azure data set mapping object</span></span>


```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4d37c-120">-Name</span><span class="sxs-lookup"><span data-stu-id="4d37c-120">-Name</span></span>
<span data-ttu-id="4d37c-121">Name der Azure-Daten satzzuordnung</span><span class="sxs-lookup"><span data-stu-id="4d37c-121">Azure data set mapping name</span></span>

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

### <span data-ttu-id="4d37c-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4d37c-122">-PassThru</span></span>
<span data-ttu-id="4d37c-123">Objekt zurückgeben (sofern angegeben).</span><span class="sxs-lookup"><span data-stu-id="4d37c-123">Return object (if specified).</span></span>

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

### <span data-ttu-id="4d37c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d37c-124">-ResourceGroupName</span></span>
<span data-ttu-id="4d37c-125">Der Name der Ressourcengruppe des Azure Data Share-Kontos</span><span class="sxs-lookup"><span data-stu-id="4d37c-125">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="4d37c-126">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="4d37c-126">-ResourceId</span></span>
<span data-ttu-id="4d37c-127">Die Ressourcen-ID der Azure-Daten satzzuordnung</span><span class="sxs-lookup"><span data-stu-id="4d37c-127">The resource id of the azure data set mapping</span></span>

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

### <span data-ttu-id="4d37c-128">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="4d37c-128">-ShareSubscriptionName</span></span>
<span data-ttu-id="4d37c-129">Name des Azure Data Share-Abonnements</span><span class="sxs-lookup"><span data-stu-id="4d37c-129">Azure data share subscription name</span></span>

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

### <span data-ttu-id="4d37c-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="4d37c-130">-Confirm</span></span>
<span data-ttu-id="4d37c-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4d37c-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4d37c-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d37c-132">-WhatIf</span></span>
<span data-ttu-id="4d37c-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4d37c-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4d37c-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4d37c-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4d37c-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d37c-135">CommonParameters</span></span>
<span data-ttu-id="4d37c-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d37c-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d37c-137">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d37c-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d37c-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4d37c-138">INPUTS</span></span>

### <span data-ttu-id="4d37c-139">System. String</span><span class="sxs-lookup"><span data-stu-id="4d37c-139">System.String</span></span>

### <span data-ttu-id="4d37c-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping</span><span class="sxs-lookup"><span data-stu-id="4d37c-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping</span></span>

## <span data-ttu-id="4d37c-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4d37c-141">OUTPUTS</span></span>

### <span data-ttu-id="4d37c-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4d37c-142">System.Boolean</span></span>

## <span data-ttu-id="4d37c-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="4d37c-143">NOTES</span></span>

## <span data-ttu-id="4d37c-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4d37c-144">RELATED LINKS</span></span>
