---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azdiagnosticsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzDiagnosticSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzDiagnosticSetting.md
ms.openlocfilehash: f165396d5b3af823d91e7c06d2f1cb93eb2eaafd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94009186"
---
# <span data-ttu-id="4df4b-101">Remove-AzDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="4df4b-101">Remove-AzDiagnosticSetting</span></span>

## <span data-ttu-id="4df4b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4df4b-102">SYNOPSIS</span></span>
<span data-ttu-id="4df4b-103">Entfernen Sie eine Diagnose Einstellung für die a-Ressource.</span><span class="sxs-lookup"><span data-stu-id="4df4b-103">Remove a diagnostic setting for the a resource.</span></span>

## <span data-ttu-id="4df4b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4df4b-104">SYNTAX</span></span>

```
Remove-AzDiagnosticSetting -ResourceId <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4df4b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4df4b-105">DESCRIPTION</span></span>
<span data-ttu-id="4df4b-106">Das Cmdlet **Remove-AzDiagnosticSetting** entfernt die Diagnose Einstellung für die jeweilige Ressource.</span><span class="sxs-lookup"><span data-stu-id="4df4b-106">The **Remove-AzDiagnosticSetting** cmdlet removes the diagnostic setting for the particular resource.</span></span>
<span data-ttu-id="4df4b-107">Dieses Cmdlet implementiert das ShouldProcess-Muster, d. h., es kann eine Bestätigung des Benutzers anfordern, bevor die Ressource tatsächlich erstellt, geändert oder entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="4df4b-107">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="4df4b-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4df4b-108">EXAMPLES</span></span>

### <span data-ttu-id="4df4b-109">Beispiel 1: Entfernen der Standard Diagnose Einstellung (Dienst) für eine Ressource</span><span class="sxs-lookup"><span data-stu-id="4df4b-109">Example 1: Remove the default diagnostic setting (service) for a resource</span></span>
```
PS C:\>Remove-AzDiagnosticSetting -ResourceId "Resource01"
```

<span data-ttu-id="4df4b-110">Dieser Befehl entfernt die Standard Diagnose Einstellung (Dienst) für die Ressource namens Resource01.</span><span class="sxs-lookup"><span data-stu-id="4df4b-110">This command removes the default diagnostic setting (service) for the resource called Resource01.</span></span>

### <span data-ttu-id="4df4b-111">Beispiel 2: Entfernen der Standard Diagnose Einstellung, die durch den angegebenen Namen für eine Ressource identifiziert wird</span><span class="sxs-lookup"><span data-stu-id="4df4b-111">Example 2: Remove the default diagnostic setting identified by the given name for a resource</span></span>
```
PS C:\>Remove-AzDiagnosticSetting -ResourceId "Resource01" -Name myDiagSetting
```

<span data-ttu-id="4df4b-112">Dieser Befehl entfernt die Diagnose Einstellung "myDiagSetting" für die Ressource mit dem Namen Resource01.</span><span class="sxs-lookup"><span data-stu-id="4df4b-112">This command removes the diagnostic setting called myDiagSetting for the resource called Resource01.</span></span>

## <span data-ttu-id="4df4b-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="4df4b-113">PARAMETERS</span></span>

### <span data-ttu-id="4df4b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4df4b-114">-DefaultProfile</span></span>
<span data-ttu-id="4df4b-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4df4b-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4df4b-116">-Name</span><span class="sxs-lookup"><span data-stu-id="4df4b-116">-Name</span></span>
<span data-ttu-id="4df4b-117">Der Name der Diagnose Einstellung.</span><span class="sxs-lookup"><span data-stu-id="4df4b-117">The name of the diagnostic setting.</span></span> <span data-ttu-id="4df4b-118">Wenn der Anruf nicht standardmäßig auf "Dienst" zurückgesetzt wird, wie es in der vorherigen API der Fall war, wird dieses Cmdlet nur alle Kategorien für Metriken/Protokolle deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="4df4b-118">If not given the call default to "service" as it was in the previous API and this cmdlet will only disable all categories for metrics/logs.</span></span>

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

### <span data-ttu-id="4df4b-119">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="4df4b-119">-ResourceId</span></span>
<span data-ttu-id="4df4b-120">Gibt die ID der Ressource an.</span><span class="sxs-lookup"><span data-stu-id="4df4b-120">Specifies the ID of the resource.</span></span>

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

### <span data-ttu-id="4df4b-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="4df4b-121">-Confirm</span></span>
<span data-ttu-id="4df4b-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4df4b-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4df4b-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4df4b-123">-WhatIf</span></span>
<span data-ttu-id="4df4b-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4df4b-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4df4b-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4df4b-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4df4b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4df4b-126">CommonParameters</span></span>
<span data-ttu-id="4df4b-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4df4b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4df4b-128">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4df4b-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4df4b-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4df4b-129">INPUTS</span></span>

### <span data-ttu-id="4df4b-130">System. String</span><span class="sxs-lookup"><span data-stu-id="4df4b-130">System.String</span></span>

## <span data-ttu-id="4df4b-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4df4b-131">OUTPUTS</span></span>

### <span data-ttu-id="4df4b-132">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="4df4b-132">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="4df4b-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="4df4b-133">NOTES</span></span>

## <span data-ttu-id="4df4b-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4df4b-134">RELATED LINKS</span></span>

<span data-ttu-id="4df4b-135">[Get-AzDiagnosticSetting](./Get-AzDiagnosticSetting.md) 
 [Satz-AzDiagnosticSetting](./Set-AzDiagnosticSetting.md)</span><span class="sxs-lookup"><span data-stu-id="4df4b-135">[Get-AzDiagnosticSetting](./Get-AzDiagnosticSetting.md)
[Set-AzDiagnosticSetting](./Set-AzDiagnosticSetting.md)</span></span>
