---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 441BC2EE-DBB7-4579-BA64-9D3042B7EBD8
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementUser.md
ms.openlocfilehash: 4c90b51a316db63bad2e5481e1b6390849d83292
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98381910"
---
# <span data-ttu-id="42078-101">Remove-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="42078-101">Remove-AzApiManagementUser</span></span>

## <span data-ttu-id="42078-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="42078-102">SYNOPSIS</span></span>
<span data-ttu-id="42078-103">Löscht einen vorhandenen Benutzer.</span><span class="sxs-lookup"><span data-stu-id="42078-103">Deletes an existing user.</span></span>

## <span data-ttu-id="42078-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="42078-104">SYNTAX</span></span>

```
Remove-AzApiManagementUser -Context <PsApiManagementContext> -UserId <String> [-DeleteSubscriptions]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="42078-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="42078-105">DESCRIPTION</span></span>
<span data-ttu-id="42078-106">Das **Cmdlet "Remove-AzApiManagementUser"** löscht einen vorhandenen Benutzer.</span><span class="sxs-lookup"><span data-stu-id="42078-106">The **Remove-AzApiManagementUser** cmdlet deletes an existing user.</span></span>

## <span data-ttu-id="42078-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="42078-107">EXAMPLES</span></span>

### <span data-ttu-id="42078-108">Beispiel 1: Löschen eines Benutzers</span><span class="sxs-lookup"><span data-stu-id="42078-108">Example 1: Delete a user</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementUser -Context $apimContext -UserId "0123456789" -Force
```

<span data-ttu-id="42078-109">Mit diesem Befehl wird ein vorhandener Benutzer gelöscht.</span><span class="sxs-lookup"><span data-stu-id="42078-109">This command deletes an existing user.</span></span>

## <span data-ttu-id="42078-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="42078-110">PARAMETERS</span></span>

### <span data-ttu-id="42078-111">-Context</span><span class="sxs-lookup"><span data-stu-id="42078-111">-Context</span></span>
<span data-ttu-id="42078-112">Gibt ein **"PsApiManagementContext"-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="42078-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="42078-113">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="42078-113">This parameter is required.</span></span>

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

### <span data-ttu-id="42078-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42078-114">-DefaultProfile</span></span>
<span data-ttu-id="42078-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="42078-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="42078-116">-DeleteSubscriptions</span><span class="sxs-lookup"><span data-stu-id="42078-116">-DeleteSubscriptions</span></span>
<span data-ttu-id="42078-117">Gibt an, ob Abonnements für das Produkt gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="42078-117">Indicates whether to delete subscriptions to the product.</span></span>
<span data-ttu-id="42078-118">Wenn dieser Parameter nicht angegeben wird und ein Abonnement vorhanden ist, wird mit diesem Cmdlet eine Ausnahme ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="42078-118">If this parameter is not specified and a subscription exists, this cmdlet throws an exception.</span></span>
<span data-ttu-id="42078-119">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="42078-119">This parameter is optional.</span></span>

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

### <span data-ttu-id="42078-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="42078-120">-PassThru</span></span>
<span data-ttu-id="42078-121">Gibt an, dass dieses Cmdlet den Wert "$Ture" (sofern erfolgreich) oder den Wert "$False" zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="42078-121">Indicates that this cmdlet returns a value of $Ture, if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="42078-122">-UserId</span><span class="sxs-lookup"><span data-stu-id="42078-122">-UserId</span></span>
<span data-ttu-id="42078-123">Gibt die ID des zu entfernenden Benutzers an.</span><span class="sxs-lookup"><span data-stu-id="42078-123">Specifies the ID of the user to remove.</span></span>

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

### <span data-ttu-id="42078-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="42078-124">-Confirm</span></span>
<span data-ttu-id="42078-125">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="42078-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="42078-126">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="42078-126">-WhatIf</span></span>
<span data-ttu-id="42078-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="42078-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="42078-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="42078-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="42078-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42078-129">CommonParameters</span></span>
<span data-ttu-id="42078-130">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42078-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42078-131">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="42078-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42078-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="42078-132">INPUTS</span></span>

### <span data-ttu-id="42078-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="42078-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="42078-134">System.String</span><span class="sxs-lookup"><span data-stu-id="42078-134">System.String</span></span>

### <span data-ttu-id="42078-135">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="42078-135">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="42078-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="42078-136">OUTPUTS</span></span>

### <span data-ttu-id="42078-137">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="42078-137">System.Boolean</span></span>

## <span data-ttu-id="42078-138">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="42078-138">NOTES</span></span>

## <span data-ttu-id="42078-139">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="42078-139">RELATED LINKS</span></span>

[<span data-ttu-id="42078-140">Get-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="42078-140">Get-AzApiManagementUser</span></span>](./Get-AzApiManagementUser.md)

[<span data-ttu-id="42078-141">New-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="42078-141">New-AzApiManagementUser</span></span>](./New-AzApiManagementUser.md)

[<span data-ttu-id="42078-142">Set-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="42078-142">Set-AzApiManagementUser</span></span>](./Set-AzApiManagementUser.md)


