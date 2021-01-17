---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azdiagnosticsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzDiagnosticSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzDiagnosticSetting.md
ms.openlocfilehash: f165396d5b3af823d91e7c06d2f1cb93eb2eaafd
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98385677"
---
# <span data-ttu-id="c4fb9-101">Remove-AzDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="c4fb9-101">Remove-AzDiagnosticSetting</span></span>

## <span data-ttu-id="c4fb9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c4fb9-102">SYNOPSIS</span></span>
<span data-ttu-id="c4fb9-103">Entfernen Sie eine Diagnoseeinstellung für eine Ressource.</span><span class="sxs-lookup"><span data-stu-id="c4fb9-103">Remove a diagnostic setting for the a resource.</span></span>

## <span data-ttu-id="c4fb9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c4fb9-104">SYNTAX</span></span>

```
Remove-AzDiagnosticSetting -ResourceId <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c4fb9-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c4fb9-105">DESCRIPTION</span></span>
<span data-ttu-id="c4fb9-106">Das **Cmdlet "Remove-AzDiagnosticSetting"** entfernt die Diagnoseeinstellung für die bestimmte Ressource.</span><span class="sxs-lookup"><span data-stu-id="c4fb9-106">The **Remove-AzDiagnosticSetting** cmdlet removes the diagnostic setting for the particular resource.</span></span>
<span data-ttu-id="c4fb9-107">Dieses Cmdlet implementiert das ShouldProcess-Muster, d. h., es kann eine Bestätigung vom Benutzer anfordern, bevor die Ressource tatsächlich erstellt, geändert oder entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="c4fb9-107">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="c4fb9-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c4fb9-108">EXAMPLES</span></span>

### <span data-ttu-id="c4fb9-109">Beispiel 1: Entfernen der Standardmäßigen Diagnoseeinstellung (Dienst) für eine Ressource</span><span class="sxs-lookup"><span data-stu-id="c4fb9-109">Example 1: Remove the default diagnostic setting (service) for a resource</span></span>
```
PS C:\>Remove-AzDiagnosticSetting -ResourceId "Resource01"
```

<span data-ttu-id="c4fb9-110">Mit diesem Befehl wird die standardmäßige Diagnoseeinstellung (Dienst) für die Ressource "Ressource01" entfernt.</span><span class="sxs-lookup"><span data-stu-id="c4fb9-110">This command removes the default diagnostic setting (service) for the resource called Resource01.</span></span>

### <span data-ttu-id="c4fb9-111">Beispiel 2: Entfernen der standardmäßigen Diagnoseeinstellung, die durch den angegebenen Namen für eine Ressource identifiziert wird</span><span class="sxs-lookup"><span data-stu-id="c4fb9-111">Example 2: Remove the default diagnostic setting identified by the given name for a resource</span></span>
```
PS C:\>Remove-AzDiagnosticSetting -ResourceId "Resource01" -Name myDiagSetting
```

<span data-ttu-id="c4fb9-112">Mit diesem Befehl wird die Diagnoseeinstellung "myDiagSetting" für die Ressource namens "Resource01" entfernt.</span><span class="sxs-lookup"><span data-stu-id="c4fb9-112">This command removes the diagnostic setting called myDiagSetting for the resource called Resource01.</span></span>

## <span data-ttu-id="c4fb9-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c4fb9-113">PARAMETERS</span></span>

### <span data-ttu-id="c4fb9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4fb9-114">-DefaultProfile</span></span>
<span data-ttu-id="c4fb9-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c4fb9-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c4fb9-116">-Name</span><span class="sxs-lookup"><span data-stu-id="c4fb9-116">-Name</span></span>
<span data-ttu-id="c4fb9-117">Der Name der Diagnoseeinstellung.</span><span class="sxs-lookup"><span data-stu-id="c4fb9-117">The name of the diagnostic setting.</span></span> <span data-ttu-id="c4fb9-118">Wenn der Aufruf nicht den Standardwert "service" wie in der vorherigen API hat, werden mit diesem Cmdlet nur alle Kategorien für Metriken/Protokolle deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="c4fb9-118">If not given the call default to "service" as it was in the previous API and this cmdlet will only disable all categories for metrics/logs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4fb9-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c4fb9-119">-ResourceId</span></span>
<span data-ttu-id="c4fb9-120">Gibt die ID der Ressource an.</span><span class="sxs-lookup"><span data-stu-id="c4fb9-120">Specifies the ID of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4fb9-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c4fb9-121">-Confirm</span></span>
<span data-ttu-id="c4fb9-122">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c4fb9-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c4fb9-123">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="c4fb9-123">-WhatIf</span></span>
<span data-ttu-id="c4fb9-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c4fb9-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c4fb9-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c4fb9-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c4fb9-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4fb9-126">CommonParameters</span></span>
<span data-ttu-id="c4fb9-127">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4fb9-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4fb9-128">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c4fb9-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4fb9-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c4fb9-129">INPUTS</span></span>

### <span data-ttu-id="c4fb9-130">System.String</span><span class="sxs-lookup"><span data-stu-id="c4fb9-130">System.String</span></span>

## <span data-ttu-id="c4fb9-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c4fb9-131">OUTPUTS</span></span>

### <span data-ttu-id="c4fb9-132">Microsoft.Azure.AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="c4fb9-132">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="c4fb9-133">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="c4fb9-133">NOTES</span></span>

## <span data-ttu-id="c4fb9-134">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="c4fb9-134">RELATED LINKS</span></span>

<span data-ttu-id="c4fb9-135">[Get-AzDiagnosticSetting](./Get-AzDiagnosticSetting.md) 
 [Set-AzDiagnosticSetting](./Set-AzDiagnosticSetting.md)</span><span class="sxs-lookup"><span data-stu-id="c4fb9-135">[Get-AzDiagnosticSetting](./Get-AzDiagnosticSetting.md)
[Set-AzDiagnosticSetting](./Set-AzDiagnosticSetting.md)</span></span>
