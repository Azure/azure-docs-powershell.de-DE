---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: F0BDB0EE-1F26-450D-9C68-34C79CE8F778
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementuserfromgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementUserFromGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementUserFromGroup.md
ms.openlocfilehash: 20c6894f91e92c6f70f5f753d26fe4d76a391e70
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93821039"
---
# <span data-ttu-id="34b5a-101">Remove-AzApiManagementUserFromGroup</span><span class="sxs-lookup"><span data-stu-id="34b5a-101">Remove-AzApiManagementUserFromGroup</span></span>

## <span data-ttu-id="34b5a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="34b5a-102">SYNOPSIS</span></span>
<span data-ttu-id="34b5a-103">Entfernt einen Benutzer aus einer Gruppe.</span><span class="sxs-lookup"><span data-stu-id="34b5a-103">Removes a user from a group.</span></span>

## <span data-ttu-id="34b5a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="34b5a-104">SYNTAX</span></span>

```
Remove-AzApiManagementUserFromGroup -Context <PsApiManagementContext> -GroupId <String> -UserId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="34b5a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="34b5a-105">DESCRIPTION</span></span>
<span data-ttu-id="34b5a-106">Das Cmdlet **Remove-AzApiManagementUserFromGroup** entfernt einen Benutzer aus einer vorhandenen Gruppe.</span><span class="sxs-lookup"><span data-stu-id="34b5a-106">The **Remove-AzApiManagementUserFromGroup** cmdlet removes a user from an existing group.</span></span>

## <span data-ttu-id="34b5a-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="34b5a-107">EXAMPLES</span></span>

### <span data-ttu-id="34b5a-108">Beispiel 1: Entfernen eines Benutzers aus einer Gruppe</span><span class="sxs-lookup"><span data-stu-id="34b5a-108">Example 1: Remove a user from a group</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementUserFromGroup -Context $apimContext -GroupId "0001" -UserId "0123456789"
```

<span data-ttu-id="34b5a-109">Dieser Befehl entfernt einen Benutzer aus einer Gruppe.</span><span class="sxs-lookup"><span data-stu-id="34b5a-109">This command removes a user from a group.</span></span>

## <span data-ttu-id="34b5a-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="34b5a-110">PARAMETERS</span></span>

### <span data-ttu-id="34b5a-111">-Context</span><span class="sxs-lookup"><span data-stu-id="34b5a-111">-Context</span></span>
<span data-ttu-id="34b5a-112">Gibt ein **PsApiManagementContext** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="34b5a-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="34b5a-113">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="34b5a-113">This parameter is required.</span></span>

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

### <span data-ttu-id="34b5a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34b5a-114">-DefaultProfile</span></span>
<span data-ttu-id="34b5a-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="34b5a-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="34b5a-116">-Gruppen-Nr</span><span class="sxs-lookup"><span data-stu-id="34b5a-116">-GroupId</span></span>
<span data-ttu-id="34b5a-117">Gibt die ID der Gruppe an, aus der ein Benutzer entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="34b5a-117">Specifies the ID of the group from which to remove a user.</span></span>

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

### <span data-ttu-id="34b5a-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="34b5a-118">-PassThru</span></span>
<span data-ttu-id="34b5a-119">Gibt an, dass dieses Cmdlet einen Wert von $true zurückgibt, wenn dies erfolgreich ist, oder einen Wert von $false, andernfalls.</span><span class="sxs-lookup"><span data-stu-id="34b5a-119">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="34b5a-120">-UserID</span><span class="sxs-lookup"><span data-stu-id="34b5a-120">-UserId</span></span>
<span data-ttu-id="34b5a-121">Gibt die ID des Benutzers an, der aus der Gruppe entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="34b5a-121">Specifies the ID of the user to remove from the group.</span></span>

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

### <span data-ttu-id="34b5a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34b5a-122">CommonParameters</span></span>
<span data-ttu-id="34b5a-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34b5a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34b5a-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34b5a-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34b5a-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="34b5a-125">INPUTS</span></span>

### <span data-ttu-id="34b5a-126">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="34b5a-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="34b5a-127">System. String</span><span class="sxs-lookup"><span data-stu-id="34b5a-127">System.String</span></span>

### <span data-ttu-id="34b5a-128">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="34b5a-128">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="34b5a-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="34b5a-129">OUTPUTS</span></span>

### <span data-ttu-id="34b5a-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="34b5a-130">System.Boolean</span></span>

## <span data-ttu-id="34b5a-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="34b5a-131">NOTES</span></span>

## <span data-ttu-id="34b5a-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="34b5a-132">RELATED LINKS</span></span>

[<span data-ttu-id="34b5a-133">Add-AzApiManagementUserToGroup</span><span class="sxs-lookup"><span data-stu-id="34b5a-133">Add-AzApiManagementUserToGroup</span></span>](./Add-AzApiManagementUserToGroup.md)

[<span data-ttu-id="34b5a-134">Get-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="34b5a-134">Get-AzApiManagementUser</span></span>](./Get-AzApiManagementUser.md)


