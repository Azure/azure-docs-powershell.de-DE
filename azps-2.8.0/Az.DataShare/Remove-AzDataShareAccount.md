---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatashareaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareAccount.md
ms.openlocfilehash: 4888cacfbc92a38402bab089555ac6d6e7174038
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93651401"
---
# <span data-ttu-id="74a4b-101">Remove-AzDataShareAccount</span><span class="sxs-lookup"><span data-stu-id="74a4b-101">Remove-AzDataShareAccount</span></span>

## <span data-ttu-id="74a4b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="74a4b-102">SYNOPSIS</span></span>
<span data-ttu-id="74a4b-103">Entfernt ein DataShare-Konto</span><span class="sxs-lookup"><span data-stu-id="74a4b-103">Removes a datashare account</span></span>

## <span data-ttu-id="74a4b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="74a4b-104">SYNTAX</span></span>

### <span data-ttu-id="74a4b-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="74a4b-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareAccount -ResourceGroupName <String> -Name <String> [-PassThru] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="74a4b-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="74a4b-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareAccount -ResourceId <String> [-PassThru] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="74a4b-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="74a4b-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareAccount -InputObject <PSDataShareAccount> [-PassThru] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="74a4b-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="74a4b-108">DESCRIPTION</span></span>
<span data-ttu-id="74a4b-109">Das Cmdlet **Remove-AzDataShareAccount** entfernt ein DataShare-Konto.</span><span class="sxs-lookup"><span data-stu-id="74a4b-109">The **Remove-AzDataShareAccount** cmdlet removes a datashare account.</span></span>

## <span data-ttu-id="74a4b-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="74a4b-110">EXAMPLES</span></span>

### <span data-ttu-id="74a4b-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="74a4b-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareAccount -Name "WikiADS" -ResourceGroupName "ADS"
Confirm
Are you sure you want to remove datashare account 'WikiADS' in resource group 'ADS'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="74a4b-112">Mit diesem Befehl wird das DataShare-Kontonamens WikiADS aus der Ressourcengruppe ADS entfernt.</span><span class="sxs-lookup"><span data-stu-id="74a4b-112">This command removes the datashare account named WikiADS from the resource group named ADS.</span></span>
<span data-ttu-id="74a4b-113">Dieser Befehl gibt den Wert $true zurück.</span><span class="sxs-lookup"><span data-stu-id="74a4b-113">This command returns a value of $True.</span></span>

## <span data-ttu-id="74a4b-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="74a4b-114">PARAMETERS</span></span>

### <span data-ttu-id="74a4b-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="74a4b-115">-AsJob</span></span>
<span data-ttu-id="74a4b-116">{{Fill AsJob Description}}</span><span class="sxs-lookup"><span data-stu-id="74a4b-116">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="74a4b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74a4b-117">-DefaultProfile</span></span>
<span data-ttu-id="74a4b-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="74a4b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="74a4b-119">-Force</span><span class="sxs-lookup"><span data-stu-id="74a4b-119">-Force</span></span>
<span data-ttu-id="74a4b-120">{{Fill Force Description}}</span><span class="sxs-lookup"><span data-stu-id="74a4b-120">{{Fill Force Description}}</span></span>

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

### <span data-ttu-id="74a4b-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="74a4b-121">-InputObject</span></span>
<span data-ttu-id="74a4b-122">Das Azure-Datenfreigabe-Kontoobjekt.</span><span class="sxs-lookup"><span data-stu-id="74a4b-122">The azure data share account object.</span></span>


```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareAccount
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="74a4b-123">-Name</span><span class="sxs-lookup"><span data-stu-id="74a4b-123">-Name</span></span>
<span data-ttu-id="74a4b-124">Name des Azure Data Share-Kontos</span><span class="sxs-lookup"><span data-stu-id="74a4b-124">Azure data share account name.</span></span>

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

### <span data-ttu-id="74a4b-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="74a4b-125">-PassThru</span></span>
<span data-ttu-id="74a4b-126">Objekt zurückgeben (sofern angegeben).</span><span class="sxs-lookup"><span data-stu-id="74a4b-126">Return object (if specified).</span></span>

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

### <span data-ttu-id="74a4b-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74a4b-127">-ResourceGroupName</span></span>
<span data-ttu-id="74a4b-128">Der Name der Ressourcengruppe des Azure Data Share-Kontos.</span><span class="sxs-lookup"><span data-stu-id="74a4b-128">The resource group name of azure data share account.</span></span>

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

### <span data-ttu-id="74a4b-129">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="74a4b-129">-ResourceId</span></span>
<span data-ttu-id="74a4b-130">Die Ressourcen-ID des Azure Data Share-Kontos.</span><span class="sxs-lookup"><span data-stu-id="74a4b-130">The resource id of the azure data share account.</span></span>

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

### <span data-ttu-id="74a4b-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="74a4b-131">-Confirm</span></span>
<span data-ttu-id="74a4b-132">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="74a4b-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="74a4b-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74a4b-133">-WhatIf</span></span>
<span data-ttu-id="74a4b-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="74a4b-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="74a4b-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="74a4b-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="74a4b-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74a4b-136">CommonParameters</span></span>
<span data-ttu-id="74a4b-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74a4b-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74a4b-138">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="74a4b-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74a4b-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="74a4b-139">INPUTS</span></span>

### <span data-ttu-id="74a4b-140">System. String</span><span class="sxs-lookup"><span data-stu-id="74a4b-140">System.String</span></span>

### <span data-ttu-id="74a4b-141">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareAccount</span><span class="sxs-lookup"><span data-stu-id="74a4b-141">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareAccount</span></span>

## <span data-ttu-id="74a4b-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="74a4b-142">OUTPUTS</span></span>

### <span data-ttu-id="74a4b-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="74a4b-143">System.Boolean</span></span>

## <span data-ttu-id="74a4b-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="74a4b-144">NOTES</span></span>

## <span data-ttu-id="74a4b-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="74a4b-145">RELATED LINKS</span></span>
