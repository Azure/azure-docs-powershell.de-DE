---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationAzureActiveDirectoryApp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationAzureActiveDirectoryApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationAzureActiveDirectoryApp.md
ms.openlocfilehash: 8eec47c703290047b51ce38e97391500a9f27d74
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98302931"
---
# <span data-ttu-id="047fc-101">New-AzDataMigrationAzureActiveDirectoryApp</span><span class="sxs-lookup"><span data-stu-id="047fc-101">New-AzDataMigrationAzureActiveDirectoryApp</span></span>

## <span data-ttu-id="047fc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="047fc-102">SYNOPSIS</span></span>
<span data-ttu-id="047fc-103">Erstellen Sie eine neue Instanz von DataMigration Azure ActiveDirectory Application Details.</span><span class="sxs-lookup"><span data-stu-id="047fc-103">Create a new instance DataMigration Azure ActiveDirectory Application details.</span></span>

## <span data-ttu-id="047fc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="047fc-104">SYNTAX</span></span>

```
New-AzDataMigrationAzureActiveDirectoryApp -ApplicationId <String> -AppKey <SecureString>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="047fc-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="047fc-105">DESCRIPTION</span></span>
<span data-ttu-id="047fc-106">Erstellen Sie eine neue Instanz von DataMigration Azure ActiveDirectory Application Details.</span><span class="sxs-lookup"><span data-stu-id="047fc-106">Create a new instance DataMigration Azure ActiveDirectory Application details.</span></span>

## <span data-ttu-id="047fc-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="047fc-107">EXAMPLES</span></span>

### <span data-ttu-id="047fc-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="047fc-108">Example 1</span></span>
```powershell
PS C:\> $secpasswd = ConvertTo-SecureString "Your Secret Key Here" -AsPlainText -Force
C:\> New-AzDmsAadApp -ApplicationId "Your AppId/Service Principal ID here" -AppKey $secpasswd
```
<span data-ttu-id="047fc-109">ApplicationId: "Ihre AppId/Dienstprinzipal-ID hier" AppKey: System.Security.SecureString TenantId : "Tenant ID"</span><span class="sxs-lookup"><span data-stu-id="047fc-109">ApplicationId : "Your AppId/Service Principal Id here" AppKey        : System.Security.SecureString TenantId      : "Tenant Id"</span></span>

## <span data-ttu-id="047fc-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="047fc-110">PARAMETERS</span></span>

### <span data-ttu-id="047fc-111">-AppKey</span><span class="sxs-lookup"><span data-stu-id="047fc-111">-AppKey</span></span>
<span data-ttu-id="047fc-112">Azure Active Directory Key</span><span class="sxs-lookup"><span data-stu-id="047fc-112">Azure Active Directory Key</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases: Key

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="047fc-113">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="047fc-113">-ApplicationId</span></span>
<span data-ttu-id="047fc-114">Azure Active Directory-Anwendungs-ID</span><span class="sxs-lookup"><span data-stu-id="047fc-114">Azure Active Directory Application Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AppId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="047fc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="047fc-115">-DefaultProfile</span></span>
<span data-ttu-id="047fc-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="047fc-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="047fc-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="047fc-117">CommonParameters</span></span>
<span data-ttu-id="047fc-118">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="047fc-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="047fc-119">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="047fc-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="047fc-120">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="047fc-120">INPUTS</span></span>

### <span data-ttu-id="047fc-121">Keine</span><span class="sxs-lookup"><span data-stu-id="047fc-121">None</span></span>

## <span data-ttu-id="047fc-122">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="047fc-122">OUTPUTS</span></span>

### <span data-ttu-id="047fc-123">Microsoft.Azure.Commands.DataMigration.Models.PSAzureActiveDirectoryApp</span><span class="sxs-lookup"><span data-stu-id="047fc-123">Microsoft.Azure.Commands.DataMigration.Models.PSAzureActiveDirectoryApp</span></span>

## <span data-ttu-id="047fc-124">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="047fc-124">NOTES</span></span>

## <span data-ttu-id="047fc-125">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="047fc-125">RELATED LINKS</span></span>
