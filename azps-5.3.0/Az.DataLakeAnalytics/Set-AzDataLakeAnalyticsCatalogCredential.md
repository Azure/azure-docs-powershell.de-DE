---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: 75E4E0FB-35A8-47DA-B606-45E073D04625
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/set-azdatalakeanalyticscatalogcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsCatalogCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsCatalogCredential.md
ms.openlocfilehash: 8d188e2f19c04792ea29cadef9d9ef71c20cfce9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98472546"
---
# <span data-ttu-id="bec76-101">Set-AzDataLakeAnalyticsCatalogCredential</span><span class="sxs-lookup"><span data-stu-id="bec76-101">Set-AzDataLakeAnalyticsCatalogCredential</span></span>

## <span data-ttu-id="bec76-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bec76-102">SYNOPSIS</span></span>
<span data-ttu-id="bec76-103">Ändert das Kennwort für die Anmeldeinformationen eines Azure Data Lake Analytics-Katalogs.</span><span class="sxs-lookup"><span data-stu-id="bec76-103">Modifies an Azure Data Lake Analytics catalog credential password.</span></span>

## <span data-ttu-id="bec76-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bec76-104">SYNTAX</span></span>

### <span data-ttu-id="bec76-105">SetByHostNameAndPort (Standard)</span><span class="sxs-lookup"><span data-stu-id="bec76-105">SetByHostNameAndPort (Default)</span></span>
```
Set-AzDataLakeAnalyticsCatalogCredential [-Account] <String> [-DatabaseName] <String>
 [-CredentialName] <String> [-Credential] <PSCredential> [-NewPassword] <PSCredential> [-Uri] <Uri>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bec76-106">SetByFullURI</span><span class="sxs-lookup"><span data-stu-id="bec76-106">SetByFullURI</span></span>
```
Set-AzDataLakeAnalyticsCatalogCredential [-Account] <String> [-DatabaseName] <String>
 [-CredentialName] <String> [-Credential] <PSCredential> [-NewPassword] <PSCredential> [-DatabaseHost] <String>
 [-Port] <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bec76-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bec76-107">DESCRIPTION</span></span>
<span data-ttu-id="bec76-108">Das Set-AzDataLakeAnalyticsCatalogCredential ändert ein Anmeldeinformationskennwort, das einem Azure Data Lake Analytics-Katalog zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="bec76-108">The Set-AzDataLakeAnalyticsCatalogCredential cmdlet modifies a credential password associated with an Azure Data Lake Analytics catalog.</span></span>

## <span data-ttu-id="bec76-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="bec76-109">EXAMPLES</span></span>

### <span data-ttu-id="bec76-110">Beispiel 1: Ändern des Kennworts einer Anmeldeinformationen, die einem Konto zugeordnet ist</span><span class="sxs-lookup"><span data-stu-id="bec76-110">Example 1: Modify a credential's password associated with an account</span></span>
```
PS C:\> Set-AzDataLakeAnalyticsCatalogCredential -AccountName "ContosoAdlAccount" `
                  -DatabaseName "databaseName" `
                  -CredentialName "credName" `
                  -Credential (Get-Credential) `
                  -NewPassword (Get-Credential) `
                  -Host "example.contoso.com" -Port 8080
```

<span data-ttu-id="bec76-111">Dieser Befehl legt das Kennwort für die Anmeldeinformationen auf das in "NewPassword" angegebene Kennwort fest.</span><span class="sxs-lookup"><span data-stu-id="bec76-111">This command sets the credential password to the password specified in NewPassword.</span></span>

## <span data-ttu-id="bec76-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bec76-112">PARAMETERS</span></span>

### <span data-ttu-id="bec76-113">-Konto</span><span class="sxs-lookup"><span data-stu-id="bec76-113">-Account</span></span>
<span data-ttu-id="bec76-114">Gibt den Namen des Data Lake Analytics-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="bec76-114">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="bec76-115">-Credential</span><span class="sxs-lookup"><span data-stu-id="bec76-115">-Credential</span></span>
<span data-ttu-id="bec76-116">Gibt den Namen und das aktuelle Kennwort der Anmeldeinformationen an, die geändert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="bec76-116">Specifies the name and current password of the credential to modify.</span></span>

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

### <span data-ttu-id="bec76-117">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="bec76-117">-CredentialName</span></span>
<span data-ttu-id="bec76-118">Gibt den Namen der Anmeldeinformationen an, die geändert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="bec76-118">Specifies the name of the credential to modify</span></span>

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

### <span data-ttu-id="bec76-119">-DatabaseHost</span><span class="sxs-lookup"><span data-stu-id="bec76-119">-DatabaseHost</span></span>
<span data-ttu-id="bec76-120">Gibt den Hostnamen der externen Datenquelle an, zu der die Anmeldeinformationen im Format mydatabase.contoso.com.</span><span class="sxs-lookup"><span data-stu-id="bec76-120">Specifies the host name of the external data source the credential can connect to in the format mydatabase.contoso.com.</span></span>

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

### <span data-ttu-id="bec76-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="bec76-121">-DatabaseName</span></span>
<span data-ttu-id="bec76-122">Gibt den Namen der Datenbank im Data Lake Analytics-Konto an, das die Anmeldeinformationen enthält.</span><span class="sxs-lookup"><span data-stu-id="bec76-122">Specifies the name of the database in the Data Lake Analytics account holding the credential.</span></span>

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

### <span data-ttu-id="bec76-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bec76-123">-DefaultProfile</span></span>
<span data-ttu-id="bec76-124">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="bec76-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bec76-125">-NewPassword</span><span class="sxs-lookup"><span data-stu-id="bec76-125">-NewPassword</span></span>
<span data-ttu-id="bec76-126">Gibt das neue Kennwort für die Anmeldeinformationen an.</span><span class="sxs-lookup"><span data-stu-id="bec76-126">Specifies the new password for the credential</span></span>

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

### <span data-ttu-id="bec76-127">-Port</span><span class="sxs-lookup"><span data-stu-id="bec76-127">-Port</span></span>
<span data-ttu-id="bec76-128">Gibt die Portnummer an, die verwendet wird, um mit diesen Anmeldeinformationen eine Verbindung mit dem angegebenen DatabaseHost herzustellen.</span><span class="sxs-lookup"><span data-stu-id="bec76-128">Specifies the port number used to connect to the specified DatabaseHost using this credential.</span></span>

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

### <span data-ttu-id="bec76-129">-URI</span><span class="sxs-lookup"><span data-stu-id="bec76-129">-Uri</span></span>
<span data-ttu-id="bec76-130">Gibt den vollständigen URI (Uniform Resource Identifier) der externen Datenquelle an, mit der diese Anmeldeinformationen eine Verbindung herstellen können.</span><span class="sxs-lookup"><span data-stu-id="bec76-130">Specifies the full Uniform Resource Identifier (URI) of the external data source this credential can connect to.</span></span>

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

### <span data-ttu-id="bec76-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bec76-131">-Confirm</span></span>
<span data-ttu-id="bec76-132">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="bec76-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bec76-133">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="bec76-133">-WhatIf</span></span>
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

### <span data-ttu-id="bec76-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bec76-134">CommonParameters</span></span>
<span data-ttu-id="bec76-135">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bec76-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bec76-136">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bec76-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bec76-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="bec76-137">INPUTS</span></span>

### <span data-ttu-id="bec76-138">System.String</span><span class="sxs-lookup"><span data-stu-id="bec76-138">System.String</span></span>

### <span data-ttu-id="bec76-139">System.Management.Automation.PSCredential</span><span class="sxs-lookup"><span data-stu-id="bec76-139">System.Management.Automation.PSCredential</span></span>

### <span data-ttu-id="bec76-140">System.URI</span><span class="sxs-lookup"><span data-stu-id="bec76-140">System.Uri</span></span>

### <span data-ttu-id="bec76-141">System.Int32</span><span class="sxs-lookup"><span data-stu-id="bec76-141">System.Int32</span></span>

## <span data-ttu-id="bec76-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="bec76-142">OUTPUTS</span></span>

### <span data-ttu-id="bec76-143">Microsoft.Azure.Management.DataLake.Analytics.Models.USqlCredential</span><span class="sxs-lookup"><span data-stu-id="bec76-143">Microsoft.Azure.Management.DataLake.Analytics.Models.USqlCredential</span></span>

## <span data-ttu-id="bec76-144">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="bec76-144">NOTES</span></span>

## <span data-ttu-id="bec76-145">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="bec76-145">RELATED LINKS</span></span>
