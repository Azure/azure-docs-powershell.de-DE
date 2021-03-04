---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: 75E4E0FB-35A8-47DA-B606-45E073D04625
online version: https://docs.microsoft.com/powershell/module/az.datalakeanalytics/set-azdatalakeanalyticscatalogcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsCatalogCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsCatalogCredential.md
ms.openlocfilehash: 51af3aeffe5cf75835507e78b4638270b255fb29
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101937016"
---
# <span data-ttu-id="4d8a6-101">Set-AzDataLakeAnalyticsCatalogCredential</span><span class="sxs-lookup"><span data-stu-id="4d8a6-101">Set-AzDataLakeAnalyticsCatalogCredential</span></span>

## <span data-ttu-id="4d8a6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4d8a6-102">SYNOPSIS</span></span>
<span data-ttu-id="4d8a6-103">Ändert ein Kennwort für Azure Data Lake Analytics-Kataloganmeldeinformationen.</span><span class="sxs-lookup"><span data-stu-id="4d8a6-103">Modifies an Azure Data Lake Analytics catalog credential password.</span></span>

## <span data-ttu-id="4d8a6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4d8a6-104">SYNTAX</span></span>

### <span data-ttu-id="4d8a6-105">SetByHostNameAndPort (Standard)</span><span class="sxs-lookup"><span data-stu-id="4d8a6-105">SetByHostNameAndPort (Default)</span></span>
```
Set-AzDataLakeAnalyticsCatalogCredential [-Account] <String> [-DatabaseName] <String>
 [-CredentialName] <String> [-Credential] <PSCredential> [-NewPassword] <PSCredential> [-Uri] <Uri>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4d8a6-106">SetByFullURI</span><span class="sxs-lookup"><span data-stu-id="4d8a6-106">SetByFullURI</span></span>
```
Set-AzDataLakeAnalyticsCatalogCredential [-Account] <String> [-DatabaseName] <String>
 [-CredentialName] <String> [-Credential] <PSCredential> [-NewPassword] <PSCredential> [-DatabaseHost] <String>
 [-Port] <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4d8a6-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4d8a6-107">DESCRIPTION</span></span>
<span data-ttu-id="4d8a6-108">Das Set-AzDataLakeAnalyticsCatalogCredential cmdlet ändert ein Anmeldeinformationskennwort, das einem Azure Data Lake Analytics-Katalog zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="4d8a6-108">The Set-AzDataLakeAnalyticsCatalogCredential cmdlet modifies a credential password associated with an Azure Data Lake Analytics catalog.</span></span>

## <span data-ttu-id="4d8a6-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4d8a6-109">EXAMPLES</span></span>

### <span data-ttu-id="4d8a6-110">Beispiel 1: Ändern des Kennworts einer Anmeldeinformationen, das einem Konto zugeordnet ist</span><span class="sxs-lookup"><span data-stu-id="4d8a6-110">Example 1: Modify a credential's password associated with an account</span></span>
```
PS C:\> Set-AzDataLakeAnalyticsCatalogCredential -AccountName "ContosoAdlAccount" `
                  -DatabaseName "databaseName" `
                  -CredentialName "credName" `
                  -Credential (Get-Credential) `
                  -NewPassword (Get-Credential) `
                  -Host "example.contoso.com" -Port 8080
```

<span data-ttu-id="4d8a6-111">Mit diesem Befehl wird das Kennwort für Anmeldeinformationen auf das kennwort festgelegt, das in NewPassword angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="4d8a6-111">This command sets the credential password to the password specified in NewPassword.</span></span>

## <span data-ttu-id="4d8a6-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="4d8a6-112">PARAMETERS</span></span>

### <span data-ttu-id="4d8a6-113">-Konto</span><span class="sxs-lookup"><span data-stu-id="4d8a6-113">-Account</span></span>
<span data-ttu-id="4d8a6-114">Gibt den Namen des Data Lake Analytics-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="4d8a6-114">Specifies the Data Lake Analytics account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d8a6-115">-Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="4d8a6-115">-Credential</span></span>
<span data-ttu-id="4d8a6-116">Gibt den Namen und das aktuelle Kennwort der zu ändernden Anmeldeinformationen an.</span><span class="sxs-lookup"><span data-stu-id="4d8a6-116">Specifies the name and current password of the credential to modify.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d8a6-117">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="4d8a6-117">-CredentialName</span></span>
<span data-ttu-id="4d8a6-118">Gibt den Namen der Zu ändernden Anmeldeinformationen an.</span><span class="sxs-lookup"><span data-stu-id="4d8a6-118">Specifies the name of the credential to modify</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d8a6-119">-DatabaseHost</span><span class="sxs-lookup"><span data-stu-id="4d8a6-119">-DatabaseHost</span></span>
<span data-ttu-id="4d8a6-120">Gibt den Hostnamen der externen Datenquelle an, mit der die Anmeldeinformationen im Format mydatabase.contoso.com.</span><span class="sxs-lookup"><span data-stu-id="4d8a6-120">Specifies the host name of the external data source the credential can connect to in the format mydatabase.contoso.com.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByFullURI
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d8a6-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="4d8a6-121">-DatabaseName</span></span>
<span data-ttu-id="4d8a6-122">Gibt den Namen der Datenbank im Data Lake Analytics-Konto mit den Anmeldeinformationen an.</span><span class="sxs-lookup"><span data-stu-id="4d8a6-122">Specifies the name of the database in the Data Lake Analytics account holding the credential.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d8a6-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d8a6-123">-DefaultProfile</span></span>
<span data-ttu-id="4d8a6-124">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="4d8a6-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4d8a6-125">-NewPassword</span><span class="sxs-lookup"><span data-stu-id="4d8a6-125">-NewPassword</span></span>
<span data-ttu-id="4d8a6-126">Gibt das neue Kennwort für die Anmeldeinformationen an.</span><span class="sxs-lookup"><span data-stu-id="4d8a6-126">Specifies the new password for the credential</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d8a6-127">-Port</span><span class="sxs-lookup"><span data-stu-id="4d8a6-127">-Port</span></span>
<span data-ttu-id="4d8a6-128">Gibt die Portnummer an, die zum Herstellen einer Verbindung mit dem angegebenen DatabaseHost mithilfe dieser Anmeldeinformationen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="4d8a6-128">Specifies the port number used to connect to the specified DatabaseHost using this credential.</span></span>

```yaml
Type: System.Int32
Parameter Sets: SetByFullURI
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d8a6-129">-URI</span><span class="sxs-lookup"><span data-stu-id="4d8a6-129">-Uri</span></span>
<span data-ttu-id="4d8a6-130">Gibt den vollständigen URI (Uniform Resource Identifier) der externen Datenquelle an, mit der diese Anmeldeinformationen eine Verbindung herstellen können.</span><span class="sxs-lookup"><span data-stu-id="4d8a6-130">Specifies the full Uniform Resource Identifier (URI) of the external data source this credential can connect to.</span></span>

```yaml
Type: System.Uri
Parameter Sets: SetByHostNameAndPort
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d8a6-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="4d8a6-131">-Confirm</span></span>
<span data-ttu-id="4d8a6-132">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4d8a6-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4d8a6-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d8a6-133">-WhatIf</span></span>
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

### <span data-ttu-id="4d8a6-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d8a6-134">CommonParameters</span></span>
<span data-ttu-id="4d8a6-135">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d8a6-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d8a6-136">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d8a6-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d8a6-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4d8a6-137">INPUTS</span></span>

### <span data-ttu-id="4d8a6-138">System.String</span><span class="sxs-lookup"><span data-stu-id="4d8a6-138">System.String</span></span>

### <span data-ttu-id="4d8a6-139">System.Management.Automation.PSCredential</span><span class="sxs-lookup"><span data-stu-id="4d8a6-139">System.Management.Automation.PSCredential</span></span>

### <span data-ttu-id="4d8a6-140">System.Uri</span><span class="sxs-lookup"><span data-stu-id="4d8a6-140">System.Uri</span></span>

### <span data-ttu-id="4d8a6-141">System.Int32</span><span class="sxs-lookup"><span data-stu-id="4d8a6-141">System.Int32</span></span>

## <span data-ttu-id="4d8a6-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4d8a6-142">OUTPUTS</span></span>

### <span data-ttu-id="4d8a6-143">Microsoft.Azure.Management.DataLake.Analytics.Models.USqlCredential</span><span class="sxs-lookup"><span data-stu-id="4d8a6-143">Microsoft.Azure.Management.DataLake.Analytics.Models.USqlCredential</span></span>

## <span data-ttu-id="4d8a6-144">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="4d8a6-144">NOTES</span></span>

## <span data-ttu-id="4d8a6-145">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="4d8a6-145">RELATED LINKS</span></span>
