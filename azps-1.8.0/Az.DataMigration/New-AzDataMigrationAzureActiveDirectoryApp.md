---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationAzureActiveDirectoryApp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationAzureActiveDirectoryApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationAzureActiveDirectoryApp.md
ms.openlocfilehash: 2d7a7d61d5a29113f9b0e40340ae6b13b599115f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93661244"
---
# <span data-ttu-id="36e48-101">New-AzDataMigrationAzureActiveDirectoryApp</span><span class="sxs-lookup"><span data-stu-id="36e48-101">New-AzDataMigrationAzureActiveDirectoryApp</span></span>

## <span data-ttu-id="36e48-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="36e48-102">SYNOPSIS</span></span>
<span data-ttu-id="36e48-103">Erstellen Sie eine neue Instanz datamigration Azure ActiveDirectory-Anwendungsdetails.</span><span class="sxs-lookup"><span data-stu-id="36e48-103">Create a new instance DataMigration Azure ActiveDirectory Application details.</span></span>

## <span data-ttu-id="36e48-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="36e48-104">SYNTAX</span></span>

```
New-AzDataMigrationAzureActiveDirectoryApp -ApplicationId <String> -AppKey <SecureString>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="36e48-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="36e48-105">DESCRIPTION</span></span>
<span data-ttu-id="36e48-106">Erstellen Sie eine neue Instanz datamigration Azure ActiveDirectory-Anwendungsdetails.</span><span class="sxs-lookup"><span data-stu-id="36e48-106">Create a new instance DataMigration Azure ActiveDirectory Application details.</span></span>

## <span data-ttu-id="36e48-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="36e48-107">EXAMPLES</span></span>

### <span data-ttu-id="36e48-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="36e48-108">Example 1</span></span>
```powershell
PS C:\> $secpasswd = ConvertTo-SecureString "Your Secret Key Here" -AsPlainText -Force
C:\> New-AzDmsAadApp -ApplicationId "Your AppId/Service Principal ID here" -AppKey $secpasswd
```
<span data-ttu-id="36e48-109">ApplicationId: "Ihre Benutzerkennung/Dienstprinzipal-ID hier" AppKey: System. Security. SecureString-Mandantenkennung: "Mandanten-ID"</span><span class="sxs-lookup"><span data-stu-id="36e48-109">ApplicationId : "Your AppId/Service Principal Id here" AppKey        : System.Security.SecureString TenantId      : "Tenant Id"</span></span>

## <span data-ttu-id="36e48-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="36e48-110">PARAMETERS</span></span>

### <span data-ttu-id="36e48-111">-AppKey</span><span class="sxs-lookup"><span data-stu-id="36e48-111">-AppKey</span></span>
<span data-ttu-id="36e48-112">Azure Active Directory-Schlüssel</span><span class="sxs-lookup"><span data-stu-id="36e48-112">Azure Active Directory Key</span></span>

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

### <span data-ttu-id="36e48-113">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="36e48-113">-ApplicationId</span></span>
<span data-ttu-id="36e48-114">Azure Active Directory-Anwendungs-ID</span><span class="sxs-lookup"><span data-stu-id="36e48-114">Azure Active Directory Application Id</span></span>

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

### <span data-ttu-id="36e48-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36e48-115">-DefaultProfile</span></span>
<span data-ttu-id="36e48-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="36e48-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="36e48-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36e48-117">CommonParameters</span></span>
<span data-ttu-id="36e48-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36e48-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="36e48-119">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36e48-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36e48-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="36e48-120">INPUTS</span></span>

### <span data-ttu-id="36e48-121">Keine</span><span class="sxs-lookup"><span data-stu-id="36e48-121">None</span></span>

## <span data-ttu-id="36e48-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="36e48-122">OUTPUTS</span></span>

### <span data-ttu-id="36e48-123">Microsoft. Azure. Commands. datamigration. Models. PSAzureActiveDirectoryApp</span><span class="sxs-lookup"><span data-stu-id="36e48-123">Microsoft.Azure.Commands.DataMigration.Models.PSAzureActiveDirectoryApp</span></span>

## <span data-ttu-id="36e48-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="36e48-124">NOTES</span></span>

## <span data-ttu-id="36e48-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="36e48-125">RELATED LINKS</span></span>
