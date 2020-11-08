---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatashareinvitation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareInvitation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareInvitation.md
ms.openlocfilehash: 19347de88b1b43c41f8ce774630e92dfc3ad592c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94003075"
---
# <span data-ttu-id="5b6f2-101">Remove-AzDataShareInvitation</span><span class="sxs-lookup"><span data-stu-id="5b6f2-101">Remove-AzDataShareInvitation</span></span>

## <span data-ttu-id="5b6f2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5b6f2-102">SYNOPSIS</span></span>
<span data-ttu-id="5b6f2-103">entfernt eine Einladung</span><span class="sxs-lookup"><span data-stu-id="5b6f2-103">removes an invitation</span></span>

## <span data-ttu-id="5b6f2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5b6f2-104">SYNTAX</span></span>

### <span data-ttu-id="5b6f2-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="5b6f2-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareInvitation -ResourceGroupName <String> -AccountName <String> -ShareName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5b6f2-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5b6f2-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareInvitation -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b6f2-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5b6f2-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareInvitation -InputObject <PSDataShareInvitation> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5b6f2-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5b6f2-108">DESCRIPTION</span></span>
<span data-ttu-id="5b6f2-109">Das Cmdlet " **Remove-AzDataShareInvitation** " entfernt eine DataShare-Einladung.</span><span class="sxs-lookup"><span data-stu-id="5b6f2-109">The **Remove-AzDataShareInvitation** cmdlet removes a datashare invitation.</span></span>

## <span data-ttu-id="5b6f2-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5b6f2-110">EXAMPLES</span></span>

### <span data-ttu-id="5b6f2-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="5b6f2-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareDataSetMapping -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -Name "ADSInvite"
Are you sure you want to remove dataset mapping "ADSInvite"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="5b6f2-112">Mit diesen Befehlen wird eine Einladung mit dem Namen ADSInvite aus Freigabe AdsShare entfernt.</span><span class="sxs-lookup"><span data-stu-id="5b6f2-112">This commands removes an invitation named ADSInvite from share AdsShare.</span></span> 

## <span data-ttu-id="5b6f2-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="5b6f2-113">PARAMETERS</span></span>

### <span data-ttu-id="5b6f2-114">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="5b6f2-114">-AccountName</span></span>
<span data-ttu-id="5b6f2-115">Name des Azure-Datenfreigabe Kontos</span><span class="sxs-lookup"><span data-stu-id="5b6f2-115">Azure data share account name</span></span>

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

### <span data-ttu-id="5b6f2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b6f2-116">-DefaultProfile</span></span>
<span data-ttu-id="5b6f2-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5b6f2-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5b6f2-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="5b6f2-118">-InputObject</span></span>
<span data-ttu-id="5b6f2-119">Azure Data Freigabe-Einladungs Objekt</span><span class="sxs-lookup"><span data-stu-id="5b6f2-119">Azure data share invitation object</span></span>


```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareInvitation
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5b6f2-120">-Name</span><span class="sxs-lookup"><span data-stu-id="5b6f2-120">-Name</span></span>
<span data-ttu-id="5b6f2-121">Name der Einladung zu Azure Data Freigabe</span><span class="sxs-lookup"><span data-stu-id="5b6f2-121">Azure data share invitation name</span></span>

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

### <span data-ttu-id="5b6f2-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5b6f2-122">-PassThru</span></span>
<span data-ttu-id="5b6f2-123">Objekt zurückgeben (sofern angegeben).</span><span class="sxs-lookup"><span data-stu-id="5b6f2-123">Return object (if specified).</span></span>

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

### <span data-ttu-id="5b6f2-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b6f2-124">-ResourceGroupName</span></span>
<span data-ttu-id="5b6f2-125">Der Name der Ressourcengruppe des Azure Data Share-Kontos</span><span class="sxs-lookup"><span data-stu-id="5b6f2-125">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="5b6f2-126">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="5b6f2-126">-ResourceId</span></span>
<span data-ttu-id="5b6f2-127">Die Ressourcen-ID der Azure Data Share-Einladung</span><span class="sxs-lookup"><span data-stu-id="5b6f2-127">The resource id of the azure data share invitation</span></span>

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

### <span data-ttu-id="5b6f2-128">-Freigabename</span><span class="sxs-lookup"><span data-stu-id="5b6f2-128">-ShareName</span></span>
<span data-ttu-id="5b6f2-129">Name der Azure-Datenfreigabe.</span><span class="sxs-lookup"><span data-stu-id="5b6f2-129">Azure data share name.</span></span>

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

### <span data-ttu-id="5b6f2-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5b6f2-130">-Confirm</span></span>
<span data-ttu-id="5b6f2-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5b6f2-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5b6f2-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5b6f2-132">-WhatIf</span></span>
<span data-ttu-id="5b6f2-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5b6f2-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5b6f2-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5b6f2-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5b6f2-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b6f2-135">CommonParameters</span></span>
<span data-ttu-id="5b6f2-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b6f2-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b6f2-137">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5b6f2-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b6f2-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5b6f2-138">INPUTS</span></span>

### <span data-ttu-id="5b6f2-139">System. String</span><span class="sxs-lookup"><span data-stu-id="5b6f2-139">System.String</span></span>

### <span data-ttu-id="5b6f2-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareInvitation</span><span class="sxs-lookup"><span data-stu-id="5b6f2-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareInvitation</span></span>

## <span data-ttu-id="5b6f2-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5b6f2-141">OUTPUTS</span></span>

### <span data-ttu-id="5b6f2-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5b6f2-142">System.Boolean</span></span>

## <span data-ttu-id="5b6f2-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="5b6f2-143">NOTES</span></span>

## <span data-ttu-id="5b6f2-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5b6f2-144">RELATED LINKS</span></span>
