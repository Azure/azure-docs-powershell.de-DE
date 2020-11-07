---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/remove-azurermdiagnosticsetting
schema: 2.0.0
ms.openlocfilehash: 2555b7e5523ff739976bb30021250d684ffc6af1
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850815"
---
# <span data-ttu-id="204e3-101">Remove-AzureRmDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="204e3-101">Remove-AzureRmDiagnosticSetting</span></span>

## <span data-ttu-id="204e3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="204e3-102">SYNOPSIS</span></span>
<span data-ttu-id="204e3-103">Entfernen Sie eine Diagnose Einstellung für die a-Ressource.</span><span class="sxs-lookup"><span data-stu-id="204e3-103">Remove a diagnostic setting for the a resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="204e3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="204e3-104">SYNTAX</span></span>

```
Remove-AzureRmDiagnosticSetting -ResourceId <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="204e3-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="204e3-105">DESCRIPTION</span></span>
<span data-ttu-id="204e3-106">Das Cmdlet **Remove-AzureRmDiagnosticSetting** entfernt die Diagnose Einstellung für die jeweilige Ressource.</span><span class="sxs-lookup"><span data-stu-id="204e3-106">The **Remove-AzureRmDiagnosticSetting** cmdlet removes the diagnostic setting for the particular resource.</span></span>
<span data-ttu-id="204e3-107">Dieses Cmdlet implementiert das ShouldProcess-Muster, d. h., es kann eine Bestätigung des Benutzers anfordern, bevor die Ressource tatsächlich erstellt, geändert oder entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="204e3-107">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="204e3-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="204e3-108">EXAMPLES</span></span>

### <span data-ttu-id="204e3-109">Beispiel 1: Entfernen der Standard Diagnose Einstellung (Dienst) für eine Ressource</span><span class="sxs-lookup"><span data-stu-id="204e3-109">Example 1: Remove the default diagnostic setting (service) for a resource</span></span>
```
PS C:\>Remove-AzureRmDiagnosticSetting -ResourceId "Resource01"
```

<span data-ttu-id="204e3-110">Dieser Befehl entfernt die Standard Diagnose Einstellung (Dienst) für die Ressource namens Resource01.</span><span class="sxs-lookup"><span data-stu-id="204e3-110">This command removes the default diagnostic setting (service) for the resource called Resource01.</span></span>

### <span data-ttu-id="204e3-111">Beispiel 2: Entfernen der Standard Diagnose Einstellung, die durch den angegebenen Namen für eine Ressource identifiziert wird</span><span class="sxs-lookup"><span data-stu-id="204e3-111">Example 2: Remove the default diagnostic setting identified by the given name for a resource</span></span>
```
PS C:\>Remove-AzureRmDiagnosticSetting -ResourceId "Resource01" -Name myDiagSetting
```

<span data-ttu-id="204e3-112">Dieser Befehl entfernt die Diagnose Einstellung "myDiagSetting" für die Ressource mit dem Namen Resource01.</span><span class="sxs-lookup"><span data-stu-id="204e3-112">This command removes the diagnostic setting called myDiagSetting for the resource called Resource01.</span></span>

## <span data-ttu-id="204e3-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="204e3-113">PARAMETERS</span></span>

### <span data-ttu-id="204e3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="204e3-114">-DefaultProfile</span></span>
<span data-ttu-id="204e3-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="204e3-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="204e3-116">-Name</span><span class="sxs-lookup"><span data-stu-id="204e3-116">-Name</span></span>
<span data-ttu-id="204e3-117">Der Name der Diagnose Einstellung.</span><span class="sxs-lookup"><span data-stu-id="204e3-117">The name of the diagnostic setting.</span></span> <span data-ttu-id="204e3-118">Wenn der Anruf nicht standardmäßig auf "Dienst" zurückgesetzt wird, wie es in der vorherigen API der Fall war, wird dieses Cmdlet nur alle Kategorien für Metriken/Protokolle deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="204e3-118">If not given the call default to "service" as it was in the previous API and this cmdlet will only disable all categories for metrics/logs.</span></span>

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

### <span data-ttu-id="204e3-119">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="204e3-119">-ResourceId</span></span>
<span data-ttu-id="204e3-120">Gibt die ID der Ressource an.</span><span class="sxs-lookup"><span data-stu-id="204e3-120">Specifies the ID of the resource.</span></span>

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

### <span data-ttu-id="204e3-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="204e3-121">-Confirm</span></span>
<span data-ttu-id="204e3-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="204e3-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="204e3-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="204e3-123">-WhatIf</span></span>
<span data-ttu-id="204e3-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="204e3-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="204e3-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="204e3-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="204e3-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="204e3-126">CommonParameters</span></span>
<span data-ttu-id="204e3-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="204e3-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="204e3-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="204e3-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="204e3-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="204e3-129">INPUTS</span></span>

### <span data-ttu-id="204e3-130">System. String</span><span class="sxs-lookup"><span data-stu-id="204e3-130">System.String</span></span>

## <span data-ttu-id="204e3-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="204e3-131">OUTPUTS</span></span>

### <span data-ttu-id="204e3-132">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="204e3-132">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="204e3-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="204e3-133">NOTES</span></span>

## <span data-ttu-id="204e3-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="204e3-134">RELATED LINKS</span></span>

<span data-ttu-id="204e3-135">[Get-AzureRmDiagnosticSetting](./Get-AzureRmDiagnosticSetting.md) 
 [Satz-AzureRmDiagnosticSetting](./Set-AzureRmDiagnosticSetting.md)</span><span class="sxs-lookup"><span data-stu-id="204e3-135">[Get-AzureRmDiagnosticSetting](./Get-AzureRmDiagnosticSetting.md)
[Set-AzureRmDiagnosticSetting](./Set-AzureRmDiagnosticSetting.md)</span></span>
