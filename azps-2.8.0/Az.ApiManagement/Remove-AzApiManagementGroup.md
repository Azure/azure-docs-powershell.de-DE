---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: B88EC6DB-84AC-4F1D-AD79-0D243E0DC88A
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementGroup.md
ms.openlocfilehash: 561bec75ecfe59c65b2b8ea6ac71364573aa2bcd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93658195"
---
# <span data-ttu-id="e1669-101">Remove-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="e1669-101">Remove-AzApiManagementGroup</span></span>

## <span data-ttu-id="e1669-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e1669-102">SYNOPSIS</span></span>
<span data-ttu-id="e1669-103">Entfernt eine vorhandene API-Verwaltungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="e1669-103">Removes an existing API management group.</span></span>

## <span data-ttu-id="e1669-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e1669-104">SYNTAX</span></span>

```
Remove-AzApiManagementGroup -Context <PsApiManagementContext> -GroupId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e1669-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e1669-105">DESCRIPTION</span></span>
<span data-ttu-id="e1669-106">Das Cmdlet **Remove-AzApiManagementGroup** entfernt eine vorhandene API-Verwaltungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="e1669-106">The **Remove-AzApiManagementGroup** cmdlet removes an existing API management group.</span></span>

## <span data-ttu-id="e1669-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e1669-107">EXAMPLES</span></span>

### <span data-ttu-id="e1669-108">Beispiel 1: Entfernen einer vorhandenen Verwaltungsgruppe</span><span class="sxs-lookup"><span data-stu-id="e1669-108">Example 1: Remove an existing management group</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementGroup -Context $apimContext -GroupId "Group0001" -Force
```

<span data-ttu-id="e1669-109">Dieser Befehl entfernt eine vorhandene Verwaltungsgruppe mit dem Namen Group0001 und fordert den Benutzer nicht zur Bestätigung auf.</span><span class="sxs-lookup"><span data-stu-id="e1669-109">This command removes an existing management group named Group0001 and does not prompt the user for confirmation.</span></span>

## <span data-ttu-id="e1669-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="e1669-110">PARAMETERS</span></span>

### <span data-ttu-id="e1669-111">-Context</span><span class="sxs-lookup"><span data-stu-id="e1669-111">-Context</span></span>
<span data-ttu-id="e1669-112">Gibt die Instanz eines **PsApiManagementContext** -Objekts an.</span><span class="sxs-lookup"><span data-stu-id="e1669-112">Specifies the instance of a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e1669-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1669-113">-DefaultProfile</span></span>
<span data-ttu-id="e1669-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e1669-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e1669-115">-Gruppen-Nr</span><span class="sxs-lookup"><span data-stu-id="e1669-115">-GroupId</span></span>
<span data-ttu-id="e1669-116">Gibt den Bezeichner einer Verwaltungsgruppe an.</span><span class="sxs-lookup"><span data-stu-id="e1669-116">Specifies the identifier of a management group.</span></span>

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

### <span data-ttu-id="e1669-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e1669-117">-PassThru</span></span>
<span data-ttu-id="e1669-118">Gibt an, dass dieses Cmdlet einen Wert von $true zurückgibt, wenn es erfolgreich ist, oder einen Wert von $false, andernfalls.</span><span class="sxs-lookup"><span data-stu-id="e1669-118">Indicates that this cmdlet returns a value of $True if it succeeds, or a value of $False, otherwise.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1669-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e1669-119">-Confirm</span></span>
<span data-ttu-id="e1669-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e1669-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1669-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e1669-121">-WhatIf</span></span>
<span data-ttu-id="e1669-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e1669-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e1669-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e1669-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1669-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1669-124">CommonParameters</span></span>
<span data-ttu-id="e1669-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1669-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1669-126">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e1669-126">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1669-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e1669-127">INPUTS</span></span>

### <span data-ttu-id="e1669-128">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="e1669-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="e1669-129">System. String</span><span class="sxs-lookup"><span data-stu-id="e1669-129">System.String</span></span>

### <span data-ttu-id="e1669-130">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="e1669-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="e1669-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e1669-131">OUTPUTS</span></span>

### <span data-ttu-id="e1669-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e1669-132">System.Boolean</span></span>

## <span data-ttu-id="e1669-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="e1669-133">NOTES</span></span>

## <span data-ttu-id="e1669-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e1669-134">RELATED LINKS</span></span>

[<span data-ttu-id="e1669-135">Get-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="e1669-135">Get-AzApiManagementGroup</span></span>](./Get-AzApiManagementGroup.md)

[<span data-ttu-id="e1669-136">Neu – AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="e1669-136">New-AzApiManagementGroup</span></span>](./New-AzApiManagementGroup.md)

[<span data-ttu-id="e1669-137">Satz-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="e1669-137">Set-AzApiManagementGroup</span></span>](./Set-AzApiManagementGroup.md)


