---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/update-azalertstate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Update-AzAlertState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Update-AzAlertState.md
ms.openlocfilehash: 4ba238f75fa1e39daf2309a1ceda1aed323ff47d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94179341"
---
# <span data-ttu-id="fac40-101">Update-AzAlertState</span><span class="sxs-lookup"><span data-stu-id="fac40-101">Update-AzAlertState</span></span>

## <span data-ttu-id="fac40-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="fac40-102">SYNOPSIS</span></span>
<span data-ttu-id="fac40-103">Benachrichtigungsstatus für Updates</span><span class="sxs-lookup"><span data-stu-id="fac40-103">Updates alert state</span></span>

## <span data-ttu-id="fac40-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="fac40-104">SYNTAX</span></span>

### <span data-ttu-id="fac40-105">ByAlertId (Standard)</span><span class="sxs-lookup"><span data-stu-id="fac40-105">ByAlertId (Default)</span></span>
```
Update-AzAlertState -AlertId <String> -State <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fac40-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="fac40-106">ByInputObject</span></span>
```
Update-AzAlertState -State <String> -InputObject <PSAlert> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fac40-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fac40-107">DESCRIPTION</span></span>
<span data-ttu-id="fac40-108">**Update-AzAlertState-** Cmdlet aktualisiert den Warnungszustand.</span><span class="sxs-lookup"><span data-stu-id="fac40-108">**Update-AzAlertState** cmdlet updates alert state.</span></span>

## <span data-ttu-id="fac40-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fac40-109">EXAMPLES</span></span>

### <span data-ttu-id="fac40-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="fac40-110">Example 1</span></span>
```powershell
PS C:\> Update-AzAlertState -AlertId "afbf1b3a-0a6c-4f19-9c9b-644ccd7b1529" -State "Closed"
```

<span data-ttu-id="fac40-111">Dieses Cmdlet aktualisiert den Warnungszustand in geschlossen.</span><span class="sxs-lookup"><span data-stu-id="fac40-111">This cmdlet updates the alert state to Closed.</span></span>

## <span data-ttu-id="fac40-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="fac40-112">PARAMETERS</span></span>

### <span data-ttu-id="fac40-113">-Warnungs-Nr.</span><span class="sxs-lookup"><span data-stu-id="fac40-113">-AlertId</span></span>
<span data-ttu-id="fac40-114">Eindeutiger Bezeichner der Benachrichtigungs-ID.</span><span class="sxs-lookup"><span data-stu-id="fac40-114">Unique Identifier of Alert / ResourceId of alert.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAlertId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fac40-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fac40-115">-DefaultProfile</span></span>
<span data-ttu-id="fac40-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="fac40-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fac40-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="fac40-117">-InputObject</span></span>
<span data-ttu-id="fac40-118">Eingabeobjekt aus Pipeline.</span><span class="sxs-lookup"><span data-stu-id="fac40-118">Input object from pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlert
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fac40-119">-Bundesland</span><span class="sxs-lookup"><span data-stu-id="fac40-119">-State</span></span>
<span data-ttu-id="fac40-120">Aktualisierter Warnungsstatus</span><span class="sxs-lookup"><span data-stu-id="fac40-120">Updated Alert State</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fac40-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="fac40-121">-Confirm</span></span>
<span data-ttu-id="fac40-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="fac40-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fac40-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fac40-123">-WhatIf</span></span>
<span data-ttu-id="fac40-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fac40-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fac40-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fac40-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fac40-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fac40-126">CommonParameters</span></span>
<span data-ttu-id="fac40-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fac40-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fac40-128">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fac40-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fac40-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="fac40-129">INPUTS</span></span>

### <span data-ttu-id="fac40-130">Keine</span><span class="sxs-lookup"><span data-stu-id="fac40-130">None</span></span>

## <span data-ttu-id="fac40-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="fac40-131">OUTPUTS</span></span>

### <span data-ttu-id="fac40-132">Microsoft. Azure. Commands. AlertsManagement. OutputModels. PSAlert</span><span class="sxs-lookup"><span data-stu-id="fac40-132">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlert</span></span>

## <span data-ttu-id="fac40-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="fac40-133">NOTES</span></span>

## <span data-ttu-id="fac40-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="fac40-134">RELATED LINKS</span></span>
