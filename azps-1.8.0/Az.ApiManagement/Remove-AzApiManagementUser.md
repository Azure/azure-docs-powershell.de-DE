---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 441BC2EE-DBB7-4579-BA64-9D3042B7EBD8
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementUser.md
ms.openlocfilehash: c8c4a318f3d2e972e742afcbdc13350a0ff77a90
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93821044"
---
# <span data-ttu-id="377b8-101">Remove-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="377b8-101">Remove-AzApiManagementUser</span></span>

## <span data-ttu-id="377b8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="377b8-102">SYNOPSIS</span></span>
<span data-ttu-id="377b8-103">Löscht einen vorhandenen Benutzer.</span><span class="sxs-lookup"><span data-stu-id="377b8-103">Deletes an existing user.</span></span>

## <span data-ttu-id="377b8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="377b8-104">SYNTAX</span></span>

```
Remove-AzApiManagementUser -Context <PsApiManagementContext> -UserId <String> [-DeleteSubscriptions]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="377b8-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="377b8-105">DESCRIPTION</span></span>
<span data-ttu-id="377b8-106">Das Cmdlet **Remove-AzApiManagementUser** löscht einen vorhandenen Benutzer.</span><span class="sxs-lookup"><span data-stu-id="377b8-106">The **Remove-AzApiManagementUser** cmdlet deletes an existing user.</span></span>

## <span data-ttu-id="377b8-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="377b8-107">EXAMPLES</span></span>

### <span data-ttu-id="377b8-108">Beispiel 1: Löschen eines Benutzers</span><span class="sxs-lookup"><span data-stu-id="377b8-108">Example 1: Delete a user</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementUser -Context $apimContext -UserId "0123456789" -Force
```

<span data-ttu-id="377b8-109">Dieser Befehl löscht einen vorhandenen Benutzer.</span><span class="sxs-lookup"><span data-stu-id="377b8-109">This command deletes an existing user.</span></span>

## <span data-ttu-id="377b8-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="377b8-110">PARAMETERS</span></span>

### <span data-ttu-id="377b8-111">-Context</span><span class="sxs-lookup"><span data-stu-id="377b8-111">-Context</span></span>
<span data-ttu-id="377b8-112">Gibt ein **PsApiManagementContext** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="377b8-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="377b8-113">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="377b8-113">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="377b8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="377b8-114">-DefaultProfile</span></span>
<span data-ttu-id="377b8-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="377b8-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="377b8-116">-DeleteSubscriptions</span><span class="sxs-lookup"><span data-stu-id="377b8-116">-DeleteSubscriptions</span></span>
<span data-ttu-id="377b8-117">Gibt an, ob Abonnements für das Produkt gelöscht werden sollen.</span><span class="sxs-lookup"><span data-stu-id="377b8-117">Indicates whether to delete subscriptions to the product.</span></span>
<span data-ttu-id="377b8-118">Wenn dieser Parameter nicht angegeben ist und ein Abonnement vorhanden ist, löst dieses Cmdlet eine Ausnahme aus.</span><span class="sxs-lookup"><span data-stu-id="377b8-118">If this parameter is not specified and a subscription exists, this cmdlet throws an exception.</span></span>
<span data-ttu-id="377b8-119">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="377b8-119">This parameter is optional.</span></span>

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

### <span data-ttu-id="377b8-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="377b8-120">-PassThru</span></span>
<span data-ttu-id="377b8-121">Gibt an, dass dieses Cmdlet einen Wert von $Ture zurückgibt, wenn dies erfolgreich ist, oder einen Wert von $false, andernfalls.</span><span class="sxs-lookup"><span data-stu-id="377b8-121">Indicates that this cmdlet returns a value of $Ture, if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="377b8-122">-UserID</span><span class="sxs-lookup"><span data-stu-id="377b8-122">-UserId</span></span>
<span data-ttu-id="377b8-123">Gibt die ID des Benutzers an, der entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="377b8-123">Specifies the ID of the user to remove.</span></span>

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

### <span data-ttu-id="377b8-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="377b8-124">-Confirm</span></span>
<span data-ttu-id="377b8-125">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="377b8-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="377b8-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="377b8-126">-WhatIf</span></span>
<span data-ttu-id="377b8-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="377b8-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="377b8-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="377b8-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="377b8-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="377b8-129">CommonParameters</span></span>
<span data-ttu-id="377b8-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="377b8-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="377b8-131">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="377b8-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="377b8-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="377b8-132">INPUTS</span></span>

### <span data-ttu-id="377b8-133">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="377b8-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="377b8-134">System. String</span><span class="sxs-lookup"><span data-stu-id="377b8-134">System.String</span></span>

### <span data-ttu-id="377b8-135">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="377b8-135">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="377b8-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="377b8-136">OUTPUTS</span></span>

### <span data-ttu-id="377b8-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="377b8-137">System.Boolean</span></span>

## <span data-ttu-id="377b8-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="377b8-138">NOTES</span></span>

## <span data-ttu-id="377b8-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="377b8-139">RELATED LINKS</span></span>

[<span data-ttu-id="377b8-140">Get-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="377b8-140">Get-AzApiManagementUser</span></span>](./Get-AzApiManagementUser.md)

[<span data-ttu-id="377b8-141">Neu – AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="377b8-141">New-AzApiManagementUser</span></span>](./New-AzApiManagementUser.md)

[<span data-ttu-id="377b8-142">Satz-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="377b8-142">Set-AzApiManagementUser</span></span>](./Set-AzApiManagementUser.md)


