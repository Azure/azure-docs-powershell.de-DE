---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 4166119F-D26A-45A1-B040-D7B2459833D6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/set-azurermwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmWebApp.md
ms.openlocfilehash: a47f490ae77fc540f3e14708b19dade5ce4e7c3d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495570"
---
# <span data-ttu-id="c0694-101">Set-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="c0694-101">Set-AzureRmWebApp</span></span>

## <span data-ttu-id="c0694-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c0694-102">SYNOPSIS</span></span>
<span data-ttu-id="c0694-103">Ändert eine Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="c0694-103">Modifies an Azure Web App.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c0694-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c0694-104">SYNTAX</span></span>

### <span data-ttu-id="c0694-105">S1</span><span class="sxs-lookup"><span data-stu-id="c0694-105">S1</span></span>
```
Set-AzureRmWebApp [[-AppServicePlan] <String>] [[-DefaultDocuments] <String[]>]
 [[-NetFrameworkVersion] <String>] [[-PhpVersion] <String>] [[-RequestTracingEnabled] <Boolean>]
 [[-HttpLoggingEnabled] <Boolean>] [[-DetailedErrorLoggingEnabled] <Boolean>] [[-AppSettings] <Hashtable>]
 [[-ConnectionStrings] <Hashtable>]
 [[-HandlerMappings] <System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]>]
 [[-ManagedPipelineMode] <String>] [[-WebSocketsEnabled] <Boolean>] [[-Use32BitWorkerProcess] <Boolean>]
 [[-AutoSwapSlotName] <String>] [-ContainerImageName <String>] [-ContainerRegistryUrl <String>]
 [-ContainerRegistryUser <String>] [-ContainerRegistryPassword <SecureString>]
 [-EnableContainerContinuousDeployment <Boolean>] [-HostNames <String[]>] [-NumberOfWorkers <Int32>] [-AsJob]
 [-AssignIdentity <Boolean>] [-HttpsOnly <Boolean>] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c0694-106">S2</span><span class="sxs-lookup"><span data-stu-id="c0694-106">S2</span></span>
```
Set-AzureRmWebApp [[-Use32BitWorkerProcess] <Boolean>] [[-AutoSwapSlotName] <String>]
 [-NumberOfWorkers <Int32>] [-AsJob] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c0694-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c0694-107">DESCRIPTION</span></span>
<span data-ttu-id="c0694-108">Das Cmdlet " **Set-AzureRmWebApp** " legt eine Azure Web App fest.</span><span class="sxs-lookup"><span data-stu-id="c0694-108">The **Set-AzureRmWebApp** cmdlet sets an Azure Web App.</span></span>

## <span data-ttu-id="c0694-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c0694-109">EXAMPLES</span></span>

### <span data-ttu-id="c0694-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c0694-110">Example 1</span></span>
```
PS C:\> Set-AzureRmWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -HttpLoggingEnabled $true
```

<span data-ttu-id="c0694-111">Mit diesem Befehl wird HttpLoggingEnabled für Web-App-ContosoWebApp festgelegt, die mit der Ressourcengruppe Standard verknüpft sind – Web-westus</span><span class="sxs-lookup"><span data-stu-id="c0694-111">This command sets HttpLoggingEnabled to true for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="c0694-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="c0694-112">PARAMETERS</span></span>

### <span data-ttu-id="c0694-113">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="c0694-113">-AppServicePlan</span></span>
<span data-ttu-id="c0694-114">Name des App-Service Plans</span><span class="sxs-lookup"><span data-stu-id="c0694-114">App Service Plan Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0694-115">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="c0694-115">-AppSettings</span></span>
<span data-ttu-id="c0694-116">Hashtable für App-Einstellungen</span><span class="sxs-lookup"><span data-stu-id="c0694-116">App Settings HashTable</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: S1
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0694-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c0694-117">-AsJob</span></span>
<span data-ttu-id="c0694-118">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="c0694-118">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0694-119">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="c0694-119">-AssignIdentity</span></span>
<span data-ttu-id="c0694-120">Aktivieren/Deaktivieren von MSI für eine vorhandene Azure-webfunctionapp</span><span class="sxs-lookup"><span data-stu-id="c0694-120">Enable/disable MSI on an existing azure webapp or functionapp</span></span>

```yaml
Type: System.Boolean
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0694-121">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="c0694-121">-AutoSwapSlotName</span></span>
<span data-ttu-id="c0694-122">Name des Ziel Steckplatzes für den automatischen Austausch</span><span class="sxs-lookup"><span data-stu-id="c0694-122">Destination slot name for auto swap</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 15
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0694-123">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="c0694-123">-ConnectionStrings</span></span>
<span data-ttu-id="c0694-124">Hashtable für Verbindungszeichenfolgen</span><span class="sxs-lookup"><span data-stu-id="c0694-124">Connection Strings HashTable</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: S1
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0694-125">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="c0694-125">-ContainerImageName</span></span>
<span data-ttu-id="c0694-126">Name des Container Bilds</span><span class="sxs-lookup"><span data-stu-id="c0694-126">Container Image Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0694-127">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="c0694-127">-ContainerRegistryPassword</span></span>
<span data-ttu-id="c0694-128">Registrierungskennwort für private Container</span><span class="sxs-lookup"><span data-stu-id="c0694-128">Private Container Registry Password</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0694-129">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="c0694-129">-ContainerRegistryUrl</span></span>
<span data-ttu-id="c0694-130">URL des Registrierungsservers für private Container</span><span class="sxs-lookup"><span data-stu-id="c0694-130">Private Container Registry Server Url</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0694-131">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="c0694-131">-ContainerRegistryUser</span></span>
<span data-ttu-id="c0694-132">Benutzername für private Container-Registrierung</span><span class="sxs-lookup"><span data-stu-id="c0694-132">Private Container Registry Username</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0694-133">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="c0694-133">-DefaultDocuments</span></span>
<span data-ttu-id="c0694-134">Standard-Zeichenfolgen Array für Dokumente</span><span class="sxs-lookup"><span data-stu-id="c0694-134">Default Documents String Array</span></span>

```yaml
Type: System.String[]
Parameter Sets: S1
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0694-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0694-135">-DefaultProfile</span></span>
<span data-ttu-id="c0694-136">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c0694-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c0694-137">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="c0694-137">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="c0694-138">Detaillierte Fehlerprotokollierung aktiviert boolescher Wert</span><span class="sxs-lookup"><span data-stu-id="c0694-138">Detailed Error Logging Enabled Boolean</span></span>

```yaml
Type: System.Boolean
Parameter Sets: S1
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0694-139">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="c0694-139">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="c0694-140">Aktiviert/deaktiviert die Container-fortlaufende Bereitstellung webhook</span><span class="sxs-lookup"><span data-stu-id="c0694-140">Enables/Disables container continuous deployment webhook</span></span>

```yaml
Type: System.Boolean
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0694-141">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="c0694-141">-HandlerMappings</span></span>
<span data-ttu-id="c0694-142">Handler-Zuordnungen, IList</span><span class="sxs-lookup"><span data-stu-id="c0694-142">Handler Mappings IList</span></span>

```yaml
Type: System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]
Parameter Sets: S1
Aliases:

Required: False
Position: 11
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0694-143">-Hostnames</span><span class="sxs-lookup"><span data-stu-id="c0694-143">-HostNames</span></span>
<span data-ttu-id="c0694-144">Host-hostnames-Zeichenfolge Array</span><span class="sxs-lookup"><span data-stu-id="c0694-144">WebApp HostNames String Array</span></span>

```yaml
Type: System.String[]
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0694-145">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="c0694-145">-HttpLoggingEnabled</span></span>
<span data-ttu-id="c0694-146">HttpLoggingEnabled-boolescher Wert</span><span class="sxs-lookup"><span data-stu-id="c0694-146">HttpLoggingEnabled Boolean</span></span>

```yaml
Type: System.Boolean
Parameter Sets: S1
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0694-147">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="c0694-147">-HttpsOnly</span></span>
<span data-ttu-id="c0694-148">Aktivieren/Deaktivieren der Umleitung des gesamten Datenverkehrs an HTTPS auf einer vorhandenen Azure-webfunctionapp</span><span class="sxs-lookup"><span data-stu-id="c0694-148">Enable/disable redirecting all traffic to HTTPS on an existing azure webapp or functionapp</span></span>

```yaml
Type: System.Boolean
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0694-149">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="c0694-149">-ManagedPipelineMode</span></span>
<span data-ttu-id="c0694-150">Name des verwalteten Pipeline Modus</span><span class="sxs-lookup"><span data-stu-id="c0694-150">Managed Pipeline Mode Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:
Accepted values: Classic, Integrated

Required: False
Position: 12
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0694-151">-Name</span><span class="sxs-lookup"><span data-stu-id="c0694-151">-Name</span></span>
<span data-ttu-id="c0694-152">Name des Webhosts</span><span class="sxs-lookup"><span data-stu-id="c0694-152">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0694-153">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="c0694-153">-NetFrameworkVersion</span></span>
<span data-ttu-id="c0694-154">NET Framework-Version</span><span class="sxs-lookup"><span data-stu-id="c0694-154">Net Framework Version</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0694-155">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="c0694-155">-NumberOfWorkers</span></span>
<span data-ttu-id="c0694-156">Die Anzahl der Arbeitskräfte, die zugewiesen werden sollen</span><span class="sxs-lookup"><span data-stu-id="c0694-156">The number of workers to be allocated</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c0694-157">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="c0694-157">-PhpVersion</span></span>
<span data-ttu-id="c0694-158">PHP-Version</span><span class="sxs-lookup"><span data-stu-id="c0694-158">Php Version</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0694-159">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="c0694-159">-RequestTracingEnabled</span></span>
<span data-ttu-id="c0694-160">Anforderungs Ablaufverfolgung aktiviert</span><span class="sxs-lookup"><span data-stu-id="c0694-160">Request Tracing Enabled</span></span>

```yaml
Type: System.Boolean
Parameter Sets: S1
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0694-161">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0694-161">-ResourceGroupName</span></span>
<span data-ttu-id="c0694-162">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="c0694-162">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0694-163">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="c0694-163">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="c0694-164">Verwenden des 32-Bit-Workerprozess-booleschen Werts</span><span class="sxs-lookup"><span data-stu-id="c0694-164">Use 32-bit Worker Process Boolean</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 14
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0694-165">-Webbasierte</span><span class="sxs-lookup"><span data-stu-id="c0694-165">-WebApp</span></span>
<span data-ttu-id="c0694-166">Webobjekt</span><span class="sxs-lookup"><span data-stu-id="c0694-166">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c0694-167">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="c0694-167">-WebSocketsEnabled</span></span>
<span data-ttu-id="c0694-168">WebSocketsEnabled-boolescher Wert</span><span class="sxs-lookup"><span data-stu-id="c0694-168">WebSocketsEnabled Boolean</span></span>

```yaml
Type: System.Boolean
Parameter Sets: S1
Aliases:

Required: False
Position: 13
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0694-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0694-169">CommonParameters</span></span>
<span data-ttu-id="c0694-170">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0694-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0694-171">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0694-171">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0694-172">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c0694-172">INPUTS</span></span>

### <span data-ttu-id="c0694-173">System. Int32</span><span class="sxs-lookup"><span data-stu-id="c0694-173">System.Int32</span></span>
<span data-ttu-id="c0694-174">Parameter: NumberOfWorkers (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c0694-174">Parameters: NumberOfWorkers (ByValue)</span></span>

### <span data-ttu-id="c0694-175">System. String</span><span class="sxs-lookup"><span data-stu-id="c0694-175">System.String</span></span>

### <span data-ttu-id="c0694-176">Microsoft. Azure. Management. Websites. Models. Website</span><span class="sxs-lookup"><span data-stu-id="c0694-176">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="c0694-177">Parameter: webByValue</span><span class="sxs-lookup"><span data-stu-id="c0694-177">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="c0694-178">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c0694-178">OUTPUTS</span></span>

### <span data-ttu-id="c0694-179">Microsoft. Azure. Management. Websites. Models. Website</span><span class="sxs-lookup"><span data-stu-id="c0694-179">Microsoft.Azure.Management.WebSites.Models.Site</span></span>

## <span data-ttu-id="c0694-180">Notizen</span><span class="sxs-lookup"><span data-stu-id="c0694-180">NOTES</span></span>

## <span data-ttu-id="c0694-181">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c0694-181">RELATED LINKS</span></span>

[<span data-ttu-id="c0694-182">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="c0694-182">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="c0694-183">Neu – AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="c0694-183">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="c0694-184">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="c0694-184">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="c0694-185">Neustart-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="c0694-185">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="c0694-186">Anfang-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="c0694-186">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="c0694-187">Stopp-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="c0694-187">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)
