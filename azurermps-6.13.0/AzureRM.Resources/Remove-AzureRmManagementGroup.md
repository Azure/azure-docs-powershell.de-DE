---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermmanagementgroup/
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmManagementGroup.md
ms.openlocfilehash: 7f19e45f96dbeac1470fbcc67a7db319589ad390
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501974"
---
# <span data-ttu-id="1ad9c-101">Remove-AzureRmManagementGroup</span><span class="sxs-lookup"><span data-stu-id="1ad9c-101">Remove-AzureRmManagementGroup</span></span>

## <span data-ttu-id="1ad9c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1ad9c-102">SYNOPSIS</span></span>
<span data-ttu-id="1ad9c-103">Entfernt eine Verwaltungsgruppe</span><span class="sxs-lookup"><span data-stu-id="1ad9c-103">Removes a Management Group</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1ad9c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1ad9c-104">SYNTAX</span></span>

### <span data-ttu-id="1ad9c-105">GroupOperations (Standard)</span><span class="sxs-lookup"><span data-stu-id="1ad9c-105">GroupOperations (Default)</span></span>
```
Remove-AzureRmManagementGroup [-GroupName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1ad9c-106">ManagementGroupObject</span><span class="sxs-lookup"><span data-stu-id="1ad9c-106">ManagementGroupObject</span></span>
```
Remove-AzureRmManagementGroup -InputObject <PSManagementGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1ad9c-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1ad9c-107">DESCRIPTION</span></span>
<span data-ttu-id="1ad9c-108">Das Cmdlet **Remove-AzureRmManagementGroup** löscht eine Verwaltungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="1ad9c-108">The **Remove-AzureRmManagementGroup** cmdlet deletes a Management Group.</span></span>

## <span data-ttu-id="1ad9c-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1ad9c-109">EXAMPLES</span></span>

### <span data-ttu-id="1ad9c-110">Beispiel 1 – Entfernen einer Verwaltungsgruppe</span><span class="sxs-lookup"><span data-stu-id="1ad9c-110">Example 1 - Remove a Management Group</span></span>
```
PS C:\> Remove-AzureRmManagementGroup -GroupName "TestGroup"
```

### <span data-ttu-id="1ad9c-111">Beispiel 2 – Entfernen einer Verwaltungsgruppe durch Piping PSManagementGroup-Objekt</span><span class="sxs-lookup"><span data-stu-id="1ad9c-111">Example 2 - Remove a Management Group by piping PSManagementGroup Object</span></span>
```
PS C:\> Get-Remove-AzureRmManagementGroup -GroupName "TestGroup" | Remove-AzureRmManagementGroup
```

## <span data-ttu-id="1ad9c-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="1ad9c-112">PARAMETERS</span></span>

### <span data-ttu-id="1ad9c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ad9c-113">-DefaultProfile</span></span>
<span data-ttu-id="1ad9c-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1ad9c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1ad9c-115">-GroupName</span><span class="sxs-lookup"><span data-stu-id="1ad9c-115">-GroupName</span></span>
<span data-ttu-id="1ad9c-116">Verwaltungsgruppen-ID</span><span class="sxs-lookup"><span data-stu-id="1ad9c-116">Management Group Id</span></span>

```yaml
Type: System.String
Parameter Sets: GroupOperations
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ad9c-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="1ad9c-117">-InputObject</span></span>
<span data-ttu-id="1ad9c-118">Eingabeobjekt aus dem Get-Anruf</span><span class="sxs-lookup"><span data-stu-id="1ad9c-118">Input Object from the Get call</span></span>

```yaml
Type: Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup
Parameter Sets: ManagementGroupObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1ad9c-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1ad9c-119">-PassThru</span></span>
<span data-ttu-id="1ad9c-120">Zurück `true` zur erfolgreichen Ausführung</span><span class="sxs-lookup"><span data-stu-id="1ad9c-120">Return `true` on successful execution</span></span>

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

### <span data-ttu-id="1ad9c-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1ad9c-121">-Confirm</span></span>
<span data-ttu-id="1ad9c-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1ad9c-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1ad9c-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ad9c-123">-WhatIf</span></span>
<span data-ttu-id="1ad9c-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1ad9c-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1ad9c-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1ad9c-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1ad9c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ad9c-126">CommonParameters</span></span>
<span data-ttu-id="1ad9c-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ad9c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ad9c-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ad9c-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ad9c-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1ad9c-129">INPUTS</span></span>

### <span data-ttu-id="1ad9c-130">Microsoft. Azure. Commands. resources. Models. ManagementGroups. PSManagementGroup</span><span class="sxs-lookup"><span data-stu-id="1ad9c-130">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup</span></span>
<span data-ttu-id="1ad9c-131">Parameter: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="1ad9c-131">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="1ad9c-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1ad9c-132">OUTPUTS</span></span>

### <span data-ttu-id="1ad9c-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1ad9c-133">System.Boolean</span></span>

## <span data-ttu-id="1ad9c-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="1ad9c-134">NOTES</span></span>

## <span data-ttu-id="1ad9c-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1ad9c-135">RELATED LINKS</span></span>
