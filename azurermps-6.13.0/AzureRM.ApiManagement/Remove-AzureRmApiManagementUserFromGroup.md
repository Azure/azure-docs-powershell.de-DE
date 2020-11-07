---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: F0BDB0EE-1F26-450D-9C68-34C79CE8F778
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementuserfromgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementUserFromGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementUserFromGroup.md
ms.openlocfilehash: abf9cab8e7e832a6221a25aff40f4d7b7ae55d58
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663711"
---
# <span data-ttu-id="d7057-101">Remove-AzureRmApiManagementUserFromGroup</span><span class="sxs-lookup"><span data-stu-id="d7057-101">Remove-AzureRmApiManagementUserFromGroup</span></span>

## <span data-ttu-id="d7057-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d7057-102">SYNOPSIS</span></span>
<span data-ttu-id="d7057-103">Entfernt einen Benutzer aus einer Gruppe.</span><span class="sxs-lookup"><span data-stu-id="d7057-103">Removes a user from a group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d7057-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d7057-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementUserFromGroup -Context <PsApiManagementContext> -GroupId <String> -UserId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d7057-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d7057-105">DESCRIPTION</span></span>
<span data-ttu-id="d7057-106">Das Cmdlet **Remove-AzureRmApiManagementUserFromGroup** entfernt einen Benutzer aus einer vorhandenen Gruppe.</span><span class="sxs-lookup"><span data-stu-id="d7057-106">The **Remove-AzureRmApiManagementUserFromGroup** cmdlet removes a user from an existing group.</span></span>

## <span data-ttu-id="d7057-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d7057-107">EXAMPLES</span></span>

### <span data-ttu-id="d7057-108">Beispiel 1: Entfernen eines Benutzers aus einer Gruppe</span><span class="sxs-lookup"><span data-stu-id="d7057-108">Example 1: Remove a user from a group</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementUserFromGroup -Context $apimContext -GroupId "0001" -UserId "0123456789"
```

<span data-ttu-id="d7057-109">Dieser Befehl entfernt einen Benutzer aus einer Gruppe.</span><span class="sxs-lookup"><span data-stu-id="d7057-109">This command removes a user from a group.</span></span>

## <span data-ttu-id="d7057-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="d7057-110">PARAMETERS</span></span>

### <span data-ttu-id="d7057-111">-Context</span><span class="sxs-lookup"><span data-stu-id="d7057-111">-Context</span></span>
<span data-ttu-id="d7057-112">Gibt ein **PsApiManagementContext** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="d7057-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="d7057-113">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="d7057-113">This parameter is required.</span></span>

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

### <span data-ttu-id="d7057-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7057-114">-DefaultProfile</span></span>
<span data-ttu-id="d7057-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d7057-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d7057-116">-Gruppen-Nr</span><span class="sxs-lookup"><span data-stu-id="d7057-116">-GroupId</span></span>
<span data-ttu-id="d7057-117">Gibt die ID der Gruppe an, aus der ein Benutzer entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d7057-117">Specifies the ID of the group from which to remove a user.</span></span>

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

### <span data-ttu-id="d7057-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d7057-118">-PassThru</span></span>
<span data-ttu-id="d7057-119">Gibt an, dass dieses Cmdlet einen Wert von $true zurückgibt, wenn dies erfolgreich ist, oder einen Wert von $false, andernfalls.</span><span class="sxs-lookup"><span data-stu-id="d7057-119">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="d7057-120">-UserID</span><span class="sxs-lookup"><span data-stu-id="d7057-120">-UserId</span></span>
<span data-ttu-id="d7057-121">Gibt die ID des Benutzers an, der aus der Gruppe entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d7057-121">Specifies the ID of the user to remove from the group.</span></span>

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

### <span data-ttu-id="d7057-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7057-122">CommonParameters</span></span>
<span data-ttu-id="d7057-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7057-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7057-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7057-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7057-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d7057-125">INPUTS</span></span>

### <span data-ttu-id="d7057-126">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="d7057-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="d7057-127">System. String</span><span class="sxs-lookup"><span data-stu-id="d7057-127">System.String</span></span>

### <span data-ttu-id="d7057-128">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="d7057-128">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="d7057-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d7057-129">OUTPUTS</span></span>

### <span data-ttu-id="d7057-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d7057-130">System.Boolean</span></span>

## <span data-ttu-id="d7057-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="d7057-131">NOTES</span></span>

## <span data-ttu-id="d7057-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d7057-132">RELATED LINKS</span></span>

[<span data-ttu-id="d7057-133">Add-AzureRmApiManagementUserToGroup</span><span class="sxs-lookup"><span data-stu-id="d7057-133">Add-AzureRmApiManagementUserToGroup</span></span>](./Add-AzureRmApiManagementUserToGroup.md)

[<span data-ttu-id="d7057-134">Get-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="d7057-134">Get-AzureRmApiManagementUser</span></span>](./Get-AzureRmApiManagementUser.md)


